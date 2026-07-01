---
description: Configure webhooks para integrar sistemas externos aos eventos do gnrx
icon: webhook
---

# Webhooks

Webhooks permitem que sistemas externos recebam notificações em tempo real quando eventos ocorrem no gnrx. Em vez de fazer polling na API, você cadastra uma URL e o gnrx faz um `POST` para ela sempre que um evento acontecer.

## Eventos disponíveis

| Evento                     | Campo na configuração             | Quando dispara                                                                                  |
| -------------------------- | --------------------------------- | ----------------------------------------------------------------------------------------------- |
| `epi.entrega.concluida`    | `evento_epi_entrega_concluida`    | Entrega de item finalizada (direta, com assinatura obrigatória, por produto ou via solicitação) |
| `epi.devolucao.registrada` | `evento_epi_devolucao_registrada` | Devolução de item registrada (individual ou em massa)                                           |
| `epi.assinatura.concluida` | `evento_epi_assinatura_concluida` | Solicitação assinada digitalmente (individual, sessão ou entrega rápida)                        |
| `epi.solicitacao.criada`   | `evento_epi_solicitacao_criada`   | Nova solicitação de itens criada                                                                |
| `funcionario.criado`       | `evento_funcionario_criado`       | Funcionário criado (manual, via API de integração ou importação em massa)                       |
| `funcionario.atualizado`   | `evento_funcionario_atualizado`   | Dados do funcionário alterados                                                                  |
| `funcionario.inativado`    | `evento_funcionario_inativado`    | Funcionário inativado com sucesso                                                               |
| `estoque.entrada`          | `evento_estoque_entrada`          | Lote de estoque criado (por lote ou importação unitária)                                        |
| `compra.criada`            | `evento_compra_criada`            | Nova solicitação de compra criada                                                               |
| `compra.processada`        | `evento_compra_processada`        | Solicitação de compra processada (estoque gerado)                                               |
| `transferencia.criada`     | `evento_transferencia_criada`     | Nova solicitação de transferência de itens criada                                               |

## Formato da requisição recebida

O gnrx faz um `POST` para sua URL com os seguintes headers e body:

**Headers:**

```
Content-Type: application/json
X-Gnrx-Evento: epi.entrega.concluida
X-Gnrx-Signature: sha256=3b4c5d6e7f8a9b0c1d2e3f4a5b6c7d8e9f0a1b2c3d4e5f6a7b8c9d0e1f2a3b4
```

**Body (envelope padrão):**

```json
{
  "evento": "epi.entrega.concluida",
  "timestamp": "2026-06-30T14:05:00Z",
  "empresa_id": 10,
  "dados": {
    "solicitacao_id": 99,
    "funcionario_id": 55
  }
}
```

| Campo        | Tipo      | Descrição                                              |
| ------------ | --------- | ------------------------------------------------------ |
| `evento`     | `string`  | Tipo do evento (mesmo valor do header `X-Gnrx-Evento`) |
| `timestamp`  | `string`  | ISO 8601 UTC — momento do disparo                      |
| `empresa_id` | `integer` | ID da empresa que gerou o evento                       |
| `dados`      | `object`  | Payload específico do evento (veja seção abaixo)       |

Sua URL deve retornar **HTTP 2xx** para confirmar o recebimento. Qualquer outro status é registrado como `erro` e a mensagem pode ser re-entregue.

## Verificação de assinatura

O header `X-Gnrx-Signature` permite verificar que a requisição veio do gnrx e que o body não foi adulterado em trânsito.

**Algoritmo:** HMAC-SHA256 sobre o body JSON completo (como string), usando o `secret` do webhook.

**Exemplo em Node.js:**

```javascript
const crypto = require("crypto");

function verificarAssinatura(rawBody, secret, signatureHeader) {
  const assinatura = crypto
    .createHmac("sha256", secret)
    .update(rawBody, "utf8")
    .digest("hex");

  const esperado = `sha256=${assinatura}`;
  return crypto.timingSafeEqual(
    Buffer.from(esperado),
    Buffer.from(signatureHeader),
  );
}

// Exemplo com Express:
app.post(
  "/webhooks/gnrx",
  express.raw({ type: "application/json" }),
  (req, res) => {
    const signature = req.headers["x-gnrx-signature"];

    if (
      !verificarAssinatura(req.body, process.env.GNRX_WEBHOOK_SECRET, signature)
    ) {
      return res.status(401).send("Assinatura inválida");
    }

    const evento = JSON.parse(req.body);
    // processar evento...
    res.sendStatus(200);
  },
);
```

{% hint style="info" %}
**Importante:** use `express.raw()` (não `express.json()`), pois a assinatura é calculada sobre o body como string bruta. Re-serializar o JSON depois do parse pode alterar a ordem dos campos e quebrar a verificação.
{% endhint %}

**Exemplo em Python:**

```python
import hmac
import hashlib

def verificar_assinatura(raw_body: bytes, secret: str, signature_header: str) -> bool:
    mac = hmac.new(secret.encode(), raw_body, hashlib.sha256)
    esperado = f"sha256={mac.hexdigest()}"
    return hmac.compare_digest(esperado, signature_header)
```

{% hint style="info" %}
Use sempre **comparação segura contra timing attacks** (`timingSafeEqual` / `hmac.compare_digest`). Nunca compare strings com `==`.
{% endhint %}

## Payloads por evento

### `epi.entrega.concluida`

```json
{
  "evento": "epi.entrega.concluida",
  "timestamp": "2026-06-30T14:05:00Z",
  "empresa_id": 10,
  "dados": {
    "solicitacao_id": 99,
    "funcionario_id": 55
  }
}
```

### `epi.devolucao.registrada`

Devolução individual (por solicitação):

```json
{
  "evento": "epi.devolucao.registrada",
  "timestamp": "2026-06-30T14:05:00Z",
  "empresa_id": 10,
  "dados": {
    "solicitacao_id": 99,
    "solicitacao_item_id": 12,
    "item_unitario_id": 201 | null,
    "novo_estado": 0 | 2 | 3 | 4 | 5 | 6 | null
  }
}
```

Estados possíveis em `novo_estado`:

| Código | Estado       |
| ------ | ------------ |
| `0`    | Disponível   |
| `2`    | Manutenção   |
| `3`    | Inativo      |
| `4`    | Quebra       |
| `5`    | Perda        |
| `6`    | Higienização |

`null` indica que o item não teve o estado alterado.

### `epi.assinatura.concluida`

Assinatura de solicitação individual:

```json
{
  "evento": "epi.assinatura.concluida",
  "timestamp": "2026-06-30T14:05:00Z",
  "empresa_id": 10,
  "dados": {
    "solicitacao_id": 99,
    "funcionario_id": 55,
    "solicitacao_item_ids": [110, 111, 112]
  }
}
```

### `funcionario.criado`

Via interface ou importação em massa:

```json
{
  "evento": "funcionario.criado",
  "timestamp": "2026-06-30T14:05:00Z",
  "empresa_id": 10,
  "dados": {
    "funcionario_id": 301,
    "nome": "JOÃO DA SILVA",
    "codigo_integracao": "ERP-12345" | null
  }
}
```

### `funcionario.atualizado`

```json
{
  "evento": "funcionario.atualizado",
  "timestamp": "2026-06-30T14:05:00Z",
  "empresa_id": 10,
  "dados": {
    "funcionario_id": 301
  }
}
```

### `funcionario.inativado`

```json
{
  "evento": "funcionario.inativado",
  "timestamp": "2026-06-30T14:05:00Z",
  "empresa_id": 10,
  "dados": {
    "funcionario_id": 301
  }
}
```

{% hint style="info" %}
Este evento só é disparado quando a inativação é efetivada. Se o funcionário tiver itens em aberto e a inativação for bloqueada, nenhum evento é disparado.
{% endhint %}

### `estoque.entrada`

Disparado quando um lote de estoque é criado (por lote manual ou por importação de unitários).

```json
{
  "evento": "estoque.entrada",
  "timestamp": "2026-06-30T14:05:00Z",
  "empresa_id": 10,
  "dados": {
    "lote_id": 88,
    "item_id": 12,
    "nome": "Capacete de Segurança",
    "unidade_medida": "un",
    "casas_decimais": 0,
    "quantidade_total": 500,
    "variantes": [
      {
        "variacoes": { "Tamanho": "G", "Cor": "Azul" },
        "quantidade": 300
      },
      {
        "variacoes": { "Tamanho": "M", "Cor": "Azul" },
        "quantidade": 200
      }
    ]
  }
}
```

- `unidade_medida` — unidade configurada no item (ex: `"un"`, `"kg"`, `"L"`)
- `casas_decimais` — número de casas decimais para interpretar `quantidade_total` (0 = inteiro, 2 = dividir por 100, etc.)
- `variantes` — lista das combinações de variação com suas quantidades; vazio `[]` quando o item não tem variantes ou foi importado via planilha de unitários

### `compra.criada`

```json
{
  "evento": "compra.criada",
  "timestamp": "2026-06-30T14:05:00Z",
  "empresa_id": 10,
  "dados": {
    "solicitacao_compra_id": 88
  }
}
```

### `compra.processada`

```json
{
  "evento": "compra.processada",
  "timestamp": "2026-06-30T14:05:00Z",
  "empresa_id": 10,
  "dados": {
    "solicitacao_compra_id": 88
  }
}
```

### `transferencia.criada`

```json
{
  "evento": "transferencia.criada",
  "timestamp": "2026-06-30T14:05:00Z",
  "empresa_id": 10,
  "dados": {
    "transferencia_id": 33
  }
}
```

## Boas práticas

**Responda rápido.** O worker aguarda sua resposta para processar a próxima mensagem. Retorne `200` imediatamente e processe o evento de forma assíncrona na sua aplicação. Timeout configurado em 10 segundos.

**Armazene o `secret` com segurança.** Trate-o como uma senha — use variável de ambiente ou cofre de segredos. Nunca commit no código.

**Valide a assinatura sempre.** Rejeite requisições sem header `X-Gnrx-Signature` ou com assinatura inválida.

**Idempotência.** Em casos de falha de rede, o mesmo evento pode ser entregue mais de uma vez. Projete seu handler para processar duplicatas com segurança (ex: verificar se `solicitacao_id` já foi processado antes de agir).

**HTTPS obrigatório em produção.** URLs `http://` são aceitas para testes locais, mas use HTTPS em produção para garantir confidencialidade durante o transporte (a assinatura HMAC garante integridade, não confidencialidade).
