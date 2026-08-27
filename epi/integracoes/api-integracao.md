---
description: Referência da API REST de integração do gnrx para sistemas externos (ERPs)
icon: plug
layout:
  width: default
  title:
    visible: true
  description:
    visible: true
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
  metadata:
    visible: false
  tags:
    visible: true
  actions:
    visible: true
---

# API de Integração

Documentação completa da API pública de integração da GNRx (`/integracao/v1/`), para uso por sistemas externos (ERPs de clientes). Este guia complementa o Swagger interativo (`/integracao/docs/`), trazendo contexto de negócio, exemplos prontos e fluxos ponta a ponta.

## Visão geral

A API de Integração GNRx permite que sistemas externos (ERPs, sistemas de RH, plataformas de gestão de almoxarifado dos clientes) se conectem à plataforma GNRx para automatizar processos de gestão de EPIs, itens de estoque em geral (ferramentas, uniformes, produtos), riscos ocupacionais, GHEs (Grupos Homogêneos de Exposição), estrutura organizacional (setores, cargos, locais de trabalho, funcionários) e solicitações (retirada de EPI, compra, transferência entre unidades, pedidos de parceiros).

{% hint style="info" %}
**Nota de domínio**: o sistema foi originalmente construído para gestão de EPIs (Equipamentos de Proteção Individual), mas hoje cobre qualquer tipo de item controlado pela empresa — produtos, ferramentas, uniformes, equipamentos em geral. Onde você ler "EPI" ou "item", entenda como "qualquer item de estoque que a empresa controla", não apenas equipamentos de proteção.
{% endhint %}

Com esta API você pode:

* Cadastrar e gerenciar funcionários, sincronizando com seu ERP/RH.
* Consultar e gerenciar a estrutura organizacional (locais de trabalho, setores, cargos).
* Consultar e gerenciar GHEs, riscos ocupacionais vinculados e os itens obrigatórios/opcionais de cada risco.
* Consultar e cadastrar o catálogo de tipos de item e categorias de produto.
* Consultar, criar, alterar e inativar centros de estoque, e gerenciar seu vínculo com locais de trabalho.
* Consultar estoque (itens agregados, lotes de entrada, unidades individuais rastreadas) e cadastrar novos itens.
* Consultar Certificados de Aprovação (CA) na base do Ministério do Trabalho.
* Consultar solicitações de EPI, compra, transferência entre unidades e pedidos de parceiros.

## Autenticação

Toda requisição deve incluir o header:

```
X-Gnrx-Api-Key: gnrx_sua_chave_aqui
```

A chave é gerada e gerenciada no painel GNRx em **Configurações → Integrações → API**. Cada chave tem:

| Propriedade           | Descrição                                                                                                                                                                                                                                                   |
| --------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `empresa_id`          | Empresa à qual a chave pertence — toda operação é escopada a essa empresa.                                                                                                                                                                                  |
| Módulos habilitados   | Flags booleanas por domínio: `modulo_epi`, `modulo_auditoria`, `modulo_formulario`, `modulo_habilitacao`, `modulo_treinamento`. A maioria dos endpoints deste guia exige `modulo_epi = true`; se desabilitado, a API retorna **403 Forbidden**.             |
| `locais_trabalho_ids` | `null`/ausente = acesso **global** a todas as unidades da empresa. Uma lista de IDs = a chave só enxerga (e só pode escrever em) essas unidades específicas — ver [Restrição por unidade de trabalho](api-integracao.md#restrição-por-unidade-de-trabalho). |
| Limite de requisições | Requisições por minuto permitidas para essa chave — ver [Rate limiting](api-integracao.md#rate-limiting).                                                                                                                                                   |

Use o endpoint [`GET /ping`](api-integracao.md#autenticação-ping) para validar se sua chave está funcionando antes de integrar o restante do fluxo.

## Convenções gerais

### Base URL e versionamento

```
https://api.gnrx.com.br/integracao/v1/
```

A API está na versão `v1`. Mudanças que quebrem compatibilidade serão lançadas em uma nova versão de path (`v2`, etc.) — `v1` não muda de forma incompatível e, por ser uma API aberta, nenhuma versão publicada é desativada. Há também um ambiente de sandbox espelhado em `/integracao/sandbox/v1/`, com API Key de teste dedicada, para validar integrações antes de ir a produção.

Veja a [Política de Versionamento](versionamento.md) para o detalhamento de quais mudanças são compatíveis, o ciclo de vida das versões e o changelog.

### Envelope de resposta (sucesso)

Toda resposta de sucesso (exceto `204 No Content`) vem embrulhada neste formato:

```json
{
  "status": 200,
  "title": "OK",
  "data": {
    "...": "conteúdo específico do endpoint, documentado em cada seção"
  }
}
```

* `status`: mesmo valor do status HTTP da resposta.
* `title`: `"OK"` (200), `"Created"` (201), `"Accepted"` (202), etc.
* `data`: o payload do endpoint. Pode ser um objeto único, uma lista, ou uma página (ver [Paginação](api-integracao.md#paginação)).

`204 No Content` não tem corpo — usado em operações de exclusão/desvínculo/inativação bem-sucedidas.

### Paginação

Endpoints de alto volume (estoque, solicitações) aceitam paginação via query string:

| Parâmetro | Tipo    | Padrão | Máximo | Descrição                                   |
| --------- | ------- | ------ | ------ | ------------------------------------------- |
| `limit`   | integer | 50     | 200    | Quantidade máxima de registros por página.  |
| `offset`  | integer | 0      | —      | Quantos registros pular a partir do início. |

Resposta paginada (dentro do campo `data` do envelope):

```json
{
  "status": 200,
  "title": "OK",
  "data": {
    "dados": [{ "...": "um registro" }],
    "total": 1250,
    "limit": 50,
    "offset": 0
  }
}
```

Para paginar tudo, incremente `offset` em `limit` a cada chamada até `offset >= total`.

### Restrição por unidade de trabalho

Quando a API Key tem `locais_trabalho_ids` restrito a uma lista de unidades:

* **Listagens** (GHE, estoque de unitários, solicitações de EPI/compra/transferência): os resultados são filtrados automaticamente — você só recebe registros das unidades permitidas, sem precisar informar isso na requisição.
* **Detalhe/consulta de um registro específico por ID**: se o registro pertencer a uma unidade fora da lista permitida, a API retorna **404 Not Found** (não 403 — para não vazar a existência do recurso).
* **Criação/vínculo** (ex: criar GHE, vincular risco): se você informar explicitamente um `local_trabalho_id` fora da lista permitida, a API retorna **400 Bad Request**.
* Solicitações de **parceiro-empresa** não têm relação com unidade — não são afetadas por essa restrição.
* Solicitações de **transferência** (que têm unidade de origem e destino) ficam visíveis se **qualquer uma das duas** (origem ou destino) estiver na lista permitida.

{% hint style="info" %}
**Centro de Estoque**: estoque (itens unitários), solicitações de compra e solicitações de transferência não são vinculados diretamente a `local_trabalho_id` — são vinculados a `centro_estoque_id` (ver seção [Centro de Estoque](api-integracao.md#centro-de-estoque), que também permite criar/alterar/inativar centros e gerenciar esse vínculo com unidades via API). A API resolve internamente os centros de estoque associados aos `locais_trabalho_ids` da chave (via os vínculos configurados) para aplicar o mesmo filtro automático nas listagens acima. Isso é transparente para quem consome a API — mas se você comparar `centro_estoque_id` retornado com um `local_trabalho_id` do seu sistema, eles **não são o mesmo ID**.
{% endhint %}

### Rate limiting

Cada API Key tem um limite de requisições por minuto (configurável no painel). Toda resposta inclui headers informativos:

```
x-ratelimit-limit: 300
x-ratelimit-remaining: 287
x-ratelimit-reset: 42
```

Ao exceder o limite, a API retorna **429 Too Many Requests**.

### Formato de erro

Erros seguem o padrão [RFC 7807 (Problem Details)](https://www.rfc-editor.org/rfc/rfc7807), com `Content-Type: application/problem+json`:

```json
{
  "status": 400,
  "title": "Bad Request",
  "detail": "local_trabalho_id não pertence à empresa ou está inativo"
}
```

{% hint style="warning" %}
**Atenção**: o envelope de **sucesso** usa a chave `data`; o envelope de **erro** usa a chave `detail`. Não confunda os dois formatos ao implementar o parsing das respostas.
{% endhint %}

### Status codes usados na API

| Status                      | Quando ocorre                                                                                                      |
| --------------------------- | ------------------------------------------------------------------------------------------------------------------ |
| `200 OK`                    | Consulta/listagem/atualização bem-sucedida.                                                                        |
| `201 Created`               | Criação de recurso bem-sucedida.                                                                                   |
| `204 No Content`            | Exclusão/inativação/desvínculo bem-sucedido, sem corpo de resposta.                                                |
| `400 Bad Request`           | Payload inválido, referência inexistente/inativa, ou violação de regra de negócio (ex: unidade fora do permitido). |
| `401 Unauthorized`          | API Key ausente, inválida ou expirada.                                                                             |
| `403 Forbidden`             | Módulo necessário (ex: `modulo_epi`) não habilitado para a chave.                                                  |
| `404 Not Found`             | Recurso não encontrado, ou encontrado porém fora do escopo de unidades permitidas da chave.                        |
| `409 Conflict`              | Conflito de dados (ex: nome duplicado, vínculo já existente, CA duplicado).                                        |
| `429 Too Many Requests`     | Limite de requisições por minuto excedido.                                                                         |
| `500 Internal Server Error` | Erro inesperado do servidor.                                                                                       |
| `503 Service Unavailable`   | Dependência externa indisponível (ex: base de consulta de CA).                                                     |

## Referência por domínio

### Autenticação (Ping)

#### `GET /integracao/v1/ping`

Valida se a API Key fornecida é válida, ativa e não expirada. Use este endpoint para testar a conectividade antes de integrar o restante do fluxo.

**Requer módulo**: nenhum.

**Response `200`:**

```json
{
  "status": 200,
  "title": "OK",
  "data": {
    "empresa_id": 42,
    "mensagem": "Autenticado com sucesso."
  }
}
```

**Status codes**: `200`, `401`.

***

### Funcionários | Colaboradores

#### `POST /integracao/v1/funcionario`

Cria um novo funcionário vinculado à empresa autenticada, já associado a locais de trabalho, setores e cargos.

**Requer módulo**: nenhum específico (endpoint sempre disponível para a chave autenticada).

**Request body:**

```json
{
  "nome": "João da Silva",
  "cpf": "12345678901",
  "senha": "123456",
  "codigo_integracao": "EMP-001",
  "locais_trabalho": [
    {
      "local_trabalho_id": 1,
      "setores": [
        {
          "setor_id": 5,
          "cargos": [10, 11, 12]
        }
      ]
    }
  ]
}
```

| Campo               | Tipo                | Obrigatório | Descrição                                                                                                    |
| ------------------- | ------------------- | ----------- | ------------------------------------------------------------------------------------------------------------ |
| `nome`              | string (máx. 255)   | Sim         | Nome completo do funcionário.                                                                                |
| `cpf`               | string (11 dígitos) | Sim         | CPF sem pontuação.                                                                                           |
| `senha`             | string (6 dígitos)  | Sim         | Senha inicial de acesso do funcionário.                                                                      |
| `codigo_integracao` | string              | Não         | Código do funcionário no seu sistema de origem, usado para futuras operações (inativar/reativar por código). Não é devolvido na response de criação. |
| `email`              | string (máx. 255)  | Não         | E-mail do funcionário. Armazenado em minúsculas.                                                              |
| `telefone`           | string (máx. 20)   | Não         | Telefone de contato.                                                                                          |
| `data_adesao`        | string (`YYYY-MM-DD`) | Não      | Data de adesão do funcionário à empresa.                                                                      |
| `matricula`          | string (máx. 20)   | Não         | Matrícula interna do funcionário.                                                                             |
| `turno`              | string (máx. 20)   | Não         | Turno de trabalho (ex: `"Manhã"`, `"Tarde"`, `"Noite"`).                                                      |
| `empresa_terceira_id`| integer             | Não         | ID da empresa terceira à qual o funcionário pertence — deve pertencer à mesma empresa principal da chave.     |
| `ghes_ids`           | array de integer   | Não         | IDs de GHEs aos quais o funcionário é associado na criação.                                                  |
| `locais_trabalho`   | array               | Não         | Locais de trabalho, setores e cargos aos quais o funcionário é associado na criação.                         |

**Response `201`:**

```json
{
  "status": 201,
  "title": "Created",
  "data": {
    "id": 987,
    "cpf": "12345678901",
    "nome": "JOÃO DA SILVA",
    "email": null,
    "telefone": null,
    "criado_em": "2026-07-01T12:00:00Z",
    "atualizado_em": "2026-07-01T12:00:00Z",
    "situacao": 0,
    "reconhecimento_facial_cadastrado": false,
    "data_adesao": null,
    "data_encerramento": null,
    "matricula": null,
    "turno": null,
    "empresa_terceira_id": null,
    "motivo_afastamento": null,
    "data_reativacao_prevista": null,
    "retorno_automatico": false
  }
}
```

{% hint style="info" %}
`nome` e `cpf` são normalizados para maiúsculas/minúsculas no armazenamento. O `codigo_integracao` enviado na criação **não é devolvido** nesta response — ele é usado internamente para as operações de inativar/reativar por código e para o payload do webhook `funcionario.criado`.
{% endhint %}

**Status codes**: `201`, `400`, `401`, `500`.

***

#### `DELETE /integracao/v1/funcionario/{funcionario_id}`

Inativa um funcionário pelo ID interno — permanentemente (desligamento) ou temporariamente (afastamento com motivo, ex: licença médica, alistamento militar). Se o funcionário possuir itens ativos em seu nome, retorna `409` pedindo confirmação explícita. Reconhecimentos faciais associados são removidos automaticamente.

**Path params**: `funcionario_id` (integer, obrigatório).

**Request body (todos os campos opcionais):**

```json
{
  "confirmacoes": ["possui_itens_ativos"],
  "tipo_motivo": 3,
  "motivo_descricao": "Licença maternidade — retorno previsto em outubro/2026",
  "data_reativacao_prevista": "2026-10-01",
  "retorno_automatico": false
}
```

| Campo                       | Tipo             | Descrição                                                                                                              |
| ---------------------------- | ---------------- | ------------------------------------------------------------------------------------------------------------------------ |
| `confirmacoes`               | array de string  | Confirmações explícitas — ver resposta `409` abaixo.                                                                     |
| `tipo_motivo`                | integer          | `1`=Desligamento (padrão), `2`=Alistamento militar, `3`=Licença maternidade, `4`=Licença paternidade, `5`=Licença médica, `6`=Licença sem vencimento, `7`=Outro. |
| `motivo_descricao`           | string           | Detalhamento livre do motivo. Obrigatório quando `tipo_motivo = 7`.                                                       |
| `data_reativacao_prevista`   | string (`YYYY-MM-DD`) | Data prevista de retorno — apenas informativa, a não ser que `retorno_automatico = true`.                            |
| `retorno_automatico`         | boolean (padrão `false`) | Se `true`, o funcionário é reativado automaticamente na data prevista (exige `data_reativacao_prevista`).      |

**Response `204`**: sem corpo.

**Response `409` (quando confirmação é necessária):**

```json
{
  "status": 409,
  "title": "Conflict",
  "data": {
    "confirmacoes_necessarias": ["possui_itens_ativos"]
  }
}
```

**Status codes**: `204`, `400` (não encontrado), `401`, `409`, `500`.

***

#### `DELETE /integracao/v1/funcionario/codigo/{codigo_integracao}`

Igual ao endpoint acima, mas localizando o funcionário pelo `codigo_integracao` informado na criação, em vez do ID interno.

**Path params**: `codigo_integracao` (string, obrigatório, ex: `EMP-001`).

**Status codes**: `204`, `400`, `401`, `409`, `500`.

***

#### `PATCH /integracao/v1/funcionario/{funcionario_id}/reativar`

Reativa um funcionário inativo pelo ID interno. Respeita o limite contratual de funcionários ativos da empresa.

**Path params**: `funcionario_id` (integer, obrigatório).

**Response `204`**: sem corpo.

**Status codes**: `204`, `400` (não encontrado, já ativo, ou limite de funcionários atingido), `401`, `500`.

***

#### `PATCH /integracao/v1/funcionario/codigo/{codigo_integracao}/reativar`

Igual ao anterior, localizando pelo `codigo_integracao`.

**Status codes**: `204`, `400`, `401`, `500`.

***

### Locais de Trabalho | Unidades

#### `GET /integracao/v1/local-trabalho`

Retorna todos os locais de trabalho (unidades) ativos vinculados à empresa autenticada.

**Response `200`:**

```json
{
  "status": 200,
  "title": "OK",
  "data": {
    "locais_trabalho": [
      {
        "id": 1,
        "nome": "Filial São Paulo",
        "descricao": null,
        "endereco": null,
        "criado_em": "2026-01-05T09:00:00Z",
        "atualizado_em": "2026-01-05T09:00:00Z",
        "situacao": 0,
        "quantidade_funcionarios": 150,
        "quantidade_setores": 6
      }
    ],
    "total_locais_trabalho": 1,
    "permite_adicionar_unidades": true,
    "limite_unidades": 10
  }
}
```

**Status codes**: `200`, `401`, `500`.

***

### GHEs | Grupos de Exposição

GHE (Grupo Homogêneo de Exposição) agrupa funcionários que compartilham os mesmos riscos ocupacionais em uma unidade. Cada risco dentro de um GHE pode ter itens (EPIs) obrigatórios ou opcionais vinculados.

#### `GET /integracao/v1/ghe`

Lista todos os GHEs da empresa autenticada (visão resumida, sem riscos/itens).

**Response `200`:**

```json
{
  "status": 200,
  "title": "OK",
  "data": {
    "ghes": [
      {
        "id": 50,
        "nome": "GHE Produção - Turno 1",
        "descricao": "Exposição a ruído e produtos químicos",
        "local_trabalho_id": 1,
        "situacao": 0,
        "criado_em": "2026-01-10T09:00:00Z",
        "atualizado_em": "2026-01-10T09:00:00Z"
      }
    ],
    "total_ghes": 1
  }
}
```

**Status codes**: `200`, `401`, `500`.

***

#### `GET /integracao/v1/ghe/{ghe_id}`

Detalha um GHE com todos os riscos ocupacionais vinculados e, para cada risco, os itens (EPIs) obrigatórios/opcionais associados.

**Requer módulo**: `modulo_epi`. **Restrição de unidade**: sim — retorna `404` se o GHE não estiver em uma unidade permitida.

**Path params**: `ghe_id` (integer, obrigatório).

**Response `200`:**

```json
{
  "status": 200,
  "title": "OK",
  "data": {
    "id": 50,
    "nome": "GHE Produção - Turno 1",
    "descricao": "Exposição a ruído e produtos químicos",
    "local_trabalho_id": 1,
    "situacao": 0,
    "medidas_controle": "Uso obrigatório de protetor auricular e respirador",
    "codigo_integracao": "GHE-PROD-01",
    "criado_em": "2026-01-10T09:00:00Z",
    "atualizado_em": "2026-01-10T09:00:00Z",
    "riscos": [
      {
        "id": 12,
        "nome": "Ruído",
        "categoria_nome": "Físico",
        "epis": [
          {
            "epi_id": "EPI_001",
            "descricao": "Protetor Auricular Tipo Concha",
            "obrigatorio": true
          },
          {
            "epi_id": "EPI_014",
            "descricao": "Protetor Auricular Plug",
            "obrigatorio": false
          }
        ]
      }
    ]
  }
}
```

**Status codes**: `200`, `401`, `403`, `404`, `429`, `500`.

***

#### `POST /integracao/v1/ghe`

Cria um novo GHE.

**Requer módulo**: `modulo_epi`. **Restrição de unidade**: sim — `local_trabalho_id` precisa estar entre as unidades permitidas da chave.

**Request body:**

```json
{
  "nome": "GHE Produção - Turno 2",
  "local_trabalho_id": 1,
  "descricao": "Exposição a ruído",
  "medidas_controle": "Uso obrigatório de protetor auricular",
  "codigo_integracao": "GHE-PROD-02"
}
```

| Campo               | Tipo           | Obrigatório | Descrição                              |
| ------------------- | -------------- | ----------- | -------------------------------------- |
| `nome`              | string (1-255) | Sim         | Nome do GHE.                           |
| `local_trabalho_id` | integer        | Sim         | Unidade à qual o GHE pertence.         |
| `descricao`         | string         | Não         | Descrição livre.                       |
| `medidas_controle`  | string         | Não         | Medidas de controle de risco adotadas. |
| `codigo_integracao` | string         | Não         | Código de referência no seu sistema.   |

**Response `201`:**

```json
{
  "status": 201,
  "title": "Created",
  "data": {
    "id": 51,
    "nome": "GHE Produção - Turno 2",
    "descricao": "Exposição a ruído",
    "local_trabalho_id": 1,
    "situacao": 0,
    "medidas_controle": "Uso obrigatório de protetor auricular",
    "codigo_integracao": "GHE-PROD-02",
    "criado_em": "2026-07-01T12:00:00Z",
    "atualizado_em": "2026-07-01T12:00:00Z"
  }
}
```

**Status codes**: `201`, `400`, `401`, `403`, `409` (nome duplicado na unidade), `429`, `500`.

***

#### `PATCH /integracao/v1/ghe/{ghe_id}`

Atualiza parcialmente um GHE. Campos não enviados permanecem inalterados.

**Requer módulo**: `modulo_epi`. **Restrição de unidade**: sim.

**Path params**: `ghe_id` (integer, obrigatório).

**Request body (todos os campos opcionais):**

```json
{
  "descricao": "Exposição a ruído e vibração"
}
```

**Response `200`**: mesmo formato do `GheIntegracaoApiDto` do endpoint de criação, com os valores atualizados.

**Status codes**: `200`, `400`, `401`, `403`, `404`, `429`, `500`.

***

#### `POST /integracao/v1/ghe/{ghe_id}/riscos`

Vincula um risco ocupacional já cadastrado a um GHE.

**Requer módulo**: `modulo_epi`. **Restrição de unidade**: sim.

**Path params**: `ghe_id` (integer, obrigatório).

**Request body:**

```json
{
  "risco_ocupacional_id": 12
}
```

**Response `201`:**

```json
{
  "status": 201,
  "title": "Created",
  "data": {
    "ghe_id": 51,
    "risco_ocupacional_id": 12
  }
}
```

**Status codes**: `201`, `400` (risco inválido/inativo), `401`, `403`, `404`, `409` (já vinculado), `429`, `500`.

***

#### `DELETE /integracao/v1/ghe/{ghe_id}/riscos/{risco_id}`

Desvincula um risco ocupacional do GHE. Os itens vinculados àquele risco dentro do GHE também são inativados em cascata.

**Requer módulo**: `modulo_epi`. **Restrição de unidade**: sim.

**Path params**: `ghe_id`, `risco_id` (integers, obrigatórios).

**Response `204`**: sem corpo.

**Status codes**: `204`, `401`, `403`, `404`, `429`, `500`.

***

#### `POST /integracao/v1/ghe/{ghe_id}/riscos/{risco_id}/epis`

Vincula um item (EPI) a um risco já associado ao GHE, indicando se o uso é obrigatório ou opcional.

**Requer módulo**: `modulo_epi`. **Restrição de unidade**: sim.

**Path params**: `ghe_id`, `risco_id` (integers, obrigatórios).

**Request body:**

```json
{
  "epi_id": "EPI_014",
  "obrigatorio": false
}
```

**Response `201`:**

```json
{
  "status": 201,
  "title": "Created",
  "data": {
    "ghe_id": 51,
    "risco_ocupacional_id": 12,
    "epi_id": "EPI_014",
    "obrigatorio": false
  }
}
```

**Status codes**: `201`, `400` (item inválido/inativo), `401`, `403`, `404` (GHE ou risco não vinculado), `409` (já vinculado), `429`, `500`.

***

#### `DELETE /integracao/v1/ghe/{ghe_id}/riscos/{risco_id}/epis/{epi_id}`

Desvincula um item específico de um risco dentro de um GHE, sem afetar os demais itens vinculados àquele risco.

**Path params**: `ghe_id` (integer), `risco_id` (integer), `epi_id` (string) — todos obrigatórios.

**Response `204`**: sem corpo.

**Status codes**: `204`, `401`, `403`, `404`, `429`, `500`.

***

### Setores

#### `GET /integracao/v1/setor`

Lista todos os setores da empresa autenticada.

**Response `200`:**

```json
{
  "status": 200,
  "title": "OK",
  "data": {
    "setores": [
      {
        "id": 5,
        "nome": "Produção",
        "descricao": "Linha de produção",
        "situacao": 0
      }
    ],
    "total_setores": 1
  }
}
```

**Status codes**: `200`, `401`, `500`.

***

#### `POST /integracao/v1/setor`

Cria um novo setor.

**Request body:**

```json
{
  "nome": "Manutenção",
  "descricao": "Equipe de manutenção industrial",
  "codigo_integracao": "SET-002"
}
```

**Response `201`:**

```json
{
  "status": 201,
  "title": "Created",
  "data": {
    "id": 8,
    "nome": "Manutenção",
    "descricao": "Equipe de manutenção industrial",
    "situacao": 0,
    "codigo_integracao": "SET-002"
  }
}
```

**Status codes**: `201`, `400`, `401`, `429`, `500`.

***

#### `PATCH /integracao/v1/setor/{setor_id}`

Atualiza parcialmente um setor. Campos não enviados permanecem inalterados.

**Path params**: `setor_id` (integer, obrigatório).

**Request body (todos opcionais):** `{ "nome": "...", "descricao": "...", "codigo_integracao": "..." }`

**Response `200`**: setor atualizado, mesmo formato do endpoint de criação.

**Status codes**: `200`, `400`, `401`, `404`, `429`, `500`.

***

#### `DELETE /integracao/v1/setor/{setor_id}`

Inativa um setor. Não impede a inativação de setores com funcionários ou locais vinculados.

**Path params**: `setor_id` (integer, obrigatório).

**Response `204`**: sem corpo.

**Status codes**: `204`, `401`, `404`, `429`, `500`.

***

### Cargos

#### `GET /integracao/v1/cargo`

Lista todos os cargos da empresa autenticada.

**Response `200`:**

```json
{
  "status": 200,
  "title": "OK",
  "data": {
    "cargos": [{ "id": 10, "nome": "operador de produção", "situacao": 0 }],
    "total_cargos": 1
  }
}
```

**Status codes**: `200`, `401`, `500`.

***

#### `POST /integracao/v1/cargo`

Cria um novo cargo. O nome é normalizado para minúsculas.

**Request body:**

```json
{
  "nome": "Técnico de Segurança",
  "codigo_integracao": "CARGO-010"
}
```

**Response `201`:**

```json
{
  "status": 201,
  "title": "Created",
  "data": {
    "id": 25,
    "nome": "técnico de segurança",
    "situacao": 0,
    "codigo_integracao": "CARGO-010"
  }
}
```

**Status codes**: `201`, `400`, `401`, `429`, `500`.

***

#### `PATCH /integracao/v1/cargo/{cargo_id}`

Atualiza parcialmente um cargo.

**Path params**: `cargo_id` (integer, obrigatório). **Request body (opcionais)**: `nome`, `codigo_integracao`.

**Status codes**: `200`, `400`, `401`, `404`, `429`, `500`.

***

#### `DELETE /integracao/v1/cargo/{cargo_id}`

Inativa um cargo. Não impede a inativação de cargos com funcionários vinculados.

**Path params**: `cargo_id` (integer, obrigatório).

**Status codes**: `204`, `401`, `404`, `429`, `500`.

***

### Riscos Ocupacionais

#### `GET /integracao/v1/risco`

Lista o catálogo de riscos ocupacionais da empresa (inclui riscos globais do sistema, com `categoria_risco_id`/`categoria_nome` quando aplicável).

**Requer módulo**: `modulo_epi`.

**Response `200`:**

```json
{
  "status": 200,
  "title": "OK",
  "data": {
    "riscos": [
      {
        "id": 12,
        "nome": "Ruído",
        "descricao": "Exposição a níveis de ruído acima do limite de tolerância",
        "categoria_risco_id": 1,
        "categoria_nome": "Físico",
        "situacao": 0
      }
    ],
    "total_riscos": 1
  }
}
```

**Status codes**: `200`, `401`, `403`, `429`, `500`.

***

#### `POST /integracao/v1/risco`

Cria um novo risco ocupacional para a empresa.

**Requer módulo**: `modulo_epi`.

**Request body:**

```json
{
  "nome": "Vibração",
  "descricao": "Exposição a vibrações de mãos e braços",
  "categoria_risco_id": 1
}
```

**Response `201`**: mesmo formato do item da listagem acima.

**Status codes**: `201`, `400`, `401`, `403`, `429`, `500`.

***

#### `PATCH /integracao/v1/risco/{risco_id}`

Atualiza parcialmente um risco ocupacional. **Riscos globais do sistema (não pertencentes a nenhuma empresa) não podem ser alterados.**

**Path params**: `risco_id` (integer, obrigatório). **Request body (opcionais)**: `nome`, `descricao`, `categoria_risco_id`.

**Status codes**: `200`, `400` (payload inválido ou risco é global), `401`, `403`, `404`, `429`, `500`.

***

#### `DELETE /integracao/v1/risco/{risco_id}`

Inativa um risco ocupacional da empresa. **Riscos globais não podem ser inativados.** Este endpoint não replica automaticamente a inativação em cascata de itens/GHEs vinculados feita pelo painel interno — avalie os vínculos antes de inativar.

**Path params**: `risco_id` (integer, obrigatório).

**Status codes**: `204`, `400` (risco é global), `401`, `403`, `404`, `429`, `500`.

***

### Tipos de Item

Tipo de item é o catálogo de "tipos de EPI" no sentido amplo do domínio (produtos, ferramentas, uniformes, equipamentos de proteção) — cada item de estoque (ver [Estoque](api-integracao.md#estoque)) referencia um tipo de item.

#### `GET /integracao/v1/tipo-item`

Lista todos os tipos de item da empresa, ativos e inativos.

**Requer módulo**: `modulo_epi`.

**Response `200`:**

```json
{
  "status": 200,
  "title": "OK",
  "data": {
    "tipos_epi": [
      {
        "id": "EPI_001",
        "descricao": "Protetor Auricular Tipo Concha ou Plug",
        "situacao": 0,
        "categoria_produto_id": 3,
        "ordem": 1
      }
    ],
    "total_tipos_epi": 1
  }
}
```

{% hint style="warning" %}
Não há campo `nome` nem `categoria_nome` neste DTO — apenas `descricao`. `ordem` é a posição de exibição do tipo dentro da categoria no painel.
{% endhint %}

**Status codes**: `200`, `401`, `403`, `429`, `500`.

***

#### `POST /integracao/v1/tipo-item`

Cria um novo tipo de item, vinculado a uma categoria de produto já cadastrada. O `id` **não é enviado pelo cliente** — é gerado pelo servidor no formato `P{empresa_id}__{sufixo aleatório}` (ex: `P42__a1b2c3d4`).

**Requer módulo**: `modulo_epi`.

**Request body:**

```json
{
  "descricao": "Luva de Raspa para manuseio de materiais abrasivos",
  "categoria_produto_id": 5,
  "epi_id": "LUVA-01"
}
```

| Campo                  | Tipo               | Obrigatório | Descrição                                                                                     |
| ----------------------- | ------------------ | ----------- | ----------------------------------------------------------------------------------------------- |
| `descricao`             | string (1-500)     | Sim         | Descrição do tipo de item (ex: "Capacete de Segurança", "Furadeira", "Uniforme").               |
| `categoria_produto_id`  | integer            | Sim         | ID da categoria de produto à qual este tipo pertence — deve pertencer à empresa ou ser global.  |
| `epi_id`                | string (máx. 10)   | Não         | Código curto opcional de referência — **não** é o `id` retornado na response, que é sempre gerado pelo servidor. |

{% hint style="warning" %}
Não existem campos `nome` nem `codigo_integracao` neste payload.
{% endhint %}

**Response `201`**: mesmo formato do item da listagem acima.

**Status codes**: `201`, `400` (payload inválido ou `categoria_produto_id` não encontrada), `401`, `403`, `429`, `500`.

***

### Categorias de Produto

Agrupamento visual/organizacional dos tipos de item (ex: "Proteção Auditiva", "Uniformes", "Ferramentas").

#### `GET /integracao/v1/categoria-produto`

Lista todas as categorias de produto da empresa, incluindo categorias globais do sistema.

**Requer módulo**: `modulo_epi`.

**Response `200`:**

```json
{
  "status": 200,
  "title": "OK",
  "data": {
    "categorias": [
      {
        "id": 3,
        "nome": "Proteção Auditiva",
        "descricao": "Itens de proteção auditiva",
        "cor": "#2563EB",
        "icone": "headphones",
        "ativo": true
      }
    ],
    "total_categorias": 1
  }
}
```

{% hint style="warning" %}
O campo de status aqui é `ativo` (boolean) — não `situacao` como nas demais entidades da API.
{% endhint %}

**Status codes**: `200`, `401`, `403`, `429`, `500`.

***

#### `POST /integracao/v1/categoria-produto`

Cria uma nova categoria de produto.

**Requer módulo**: `modulo_epi`.

**Request body:**

```json
{
  "nome": "Uniformes",
  "descricao": "Uniformes e vestimentas de trabalho",
  "cor": "#FF0000",
  "icone": "shirt"
}
```

| Campo        | Tipo               | Obrigatório | Descrição                                  |
| ------------- | ------------------ | ----------- | --------------------------------------------- |
| `nome`        | string (1-100)     | Sim         | Nome da categoria.                            |
| `descricao`   | string             | Não         | Descrição livre.                              |
| `cor`         | string (máx. 7)    | Não         | Cor em hexadecimal (ex: `#FF0000`).           |
| `icone`       | string (máx. 50)   | Não         | Identificador do ícone exibido no painel.     |

**Response `201`**: mesmo formato do item da listagem acima.

**Status codes**: `201`, `400`, `401`, `403`, `429`, `500`.

***

### Estoque

Estoque é modelado em três níveis: **item** (cadastro agregado, ex: "Protetor Auricular X"), **lote** (entradas de estoque), e **unitário** (unidade individual rastreada por número de série, quando o item tem `controla_unitario = true`).

#### `GET /integracao/v1/estoque/item`

Lista os itens de estoque da empresa, paginado, com filtro opcional por categoria de produto.

**Requer módulo**: `modulo_epi`.

**Query params**: `limit`, `offset`, `categoria_produto_id` (integer, opcional).

**Response `200`:**

```json
{
  "status": 200,
  "title": "OK",
  "data": {
    "dados": [
      {
        "id": 100,
        "nome": "Protetor Auricular Tipo Concha 3M",
        "numero_ca": "12345",
        "epi_id": "EPI_001",
        "data_validade": null,
        "fabricante_id": 7,
        "descricao": null,
        "situacao": 0,
        "custo": 1590,
        "tempo_troca_dias": 180,
        "estoque": 340,
        "controla_unitario": true,
        "sem_devolucao": false,
        "unidade_medida": "un",
        "casas_decimais": 0
      }
    ],
    "total": 340,
    "limit": 50,
    "offset": 0
  }
}
```

{% hint style="info" %}
`custo` está em **centavos** (1590 = R$ 15,90). Não há campo `tipo_epi_nome` — o tipo de item (`epi_id`) não tem `nome`, apenas `descricao` (ver [Tipos de Item](api-integracao.md#tipos-de-item)); resolva o nome do tipo com uma chamada separada a `GET /tipo-item` se precisar exibi-lo. `estoque` é a quantidade total atual do item, somada de todos os lotes/centros de estoque.
{% endhint %}

**Status codes**: `200`, `401`, `403`, `429`, `500`.

***

#### `POST /integracao/v1/estoque/item`

Cria um novo item de estoque, vinculado a um tipo de item já cadastrado (`epi_id`). O estoque nasce zerado — entradas são feitas por lote (fora do escopo desta API por ora).

**Requer módulo**: `modulo_epi`.

**Request body:**

```json
{
  "nome": "Protetor Auricular Plug Silicone",
  "epi_id": "EPI_001",
  "descricao": "Protetor tipo plug, silicone",
  "data_validade": null,
  "numero_ca": "54321",
  "fabricante_id": 7,
  "custo": 890,
  "tempo_troca_dias": 90,
  "controla_unitario": false,
  "sem_devolucao": true,
  "unidade_medida": "un",
  "casas_decimais": 0,
  "codigo_integracao": "ITEM-PLUG-01"
}
```

| Campo               | Tipo             | Obrigatório          | Descrição                                                                                |
| ------------------- | ---------------- | -------------------- | ---------------------------------------------------------------------------------------- |
| `nome`              | string (1-255)   | Sim                  | Nome do item.                                                                            |
| `epi_id`            | string           | Sim                  | ID do tipo de item já cadastrado (ver [Tipos de Item](api-integracao.md#tipos-de-item)). |
| `descricao`         | string           | Não                  | Descrição livre.                                                                         |
| `data_validade`     | string (`YYYY-MM-DD`) | Não              | Data de validade do item, se aplicável.                                                  |
| `numero_ca`         | string (máx. 20) | Não                  | Número do Certificado de Aprovação, se aplicável.                                        |
| `fabricante_id`     | integer          | Não                  | ID do fabricante.                                                                        |
| `custo`             | integer          | Não (padrão `0`)     | Custo unitário em centavos. Não pode ser negativo.                                       |
| `tempo_troca_dias`  | integer          | Não                  | Período padrão de troca, em dias. Valores `< 1` são descartados silenciosamente (viram `null`). |
| `controla_unitario` | boolean          | Não (padrão `true`)  | Se cada unidade é rastreada individualmente por número de série.                         |
| `sem_devolucao`     | boolean          | Não (padrão `false`) | Se o item não é passível de devolução após entrega.                                      |
| `unidade_medida`    | string           | Não (padrão `"un"`)  | Unidade de medida (`un`, `par`, `cx`, `rl`, `kg`, `L`, `m³`, `g`, `mL`, etc.).            |
| `casas_decimais`    | integer          | Não (padrão `0`)     | Casas decimais para itens medidos em fração (ex: metros, litros). Não pode ser negativo.  |
| `codigo_integracao` | string           | Não                  | Código de referência no seu sistema.                                                     |

{% hint style="warning" %}
**Regras de negócio aplicadas no servidor**, além da validação de payload:

* `sem_devolucao=true` junto com `controla_unitario=true` → `400 Bad Request` (item sem devolução não pode ter controle unitário).
* `controla_unitario=true` exige `unidade_medida="un"` e `casas_decimais=0` → senão `400 Bad Request`.
* Para `unidade_medida` em `kg`, `L`, `m³`, `g`, `mL` (consumíveis fracionáveis), o servidor **força `sem_devolucao=true`**, independentemente do valor enviado.
* Para `unidade_medida` em `un`, `par`, `cx`, `rl`, `g`, `mL`, o servidor **força `casas_decimais=0`**.
  {% endhint %}

**Response `201`**: mesmo formato de um item da listagem acima.

**Status codes**: `201`, `400` (payload inválido, regra de negócio violada, ou `epi_id` não encontrado), `401`, `403`, `409` (CA duplicado nesta empresa), `429`, `500`.

***

#### `GET /integracao/v1/estoque/item/{item_epi_id}/lote`

Lista os lotes de entrada de um item de estoque, paginado.

**Requer módulo**: `modulo_epi`.

**Path params**: `item_epi_id` (integer, obrigatório). **Query params**: `limit`, `offset`.

**Response `200`:**

```json
{
  "status": 200,
  "title": "OK",
  "data": {
    "dados": [
      {
        "id": 500,
        "numero_lote": "L-2026-001",
        "data_recebimento": "2026-06-01T10:00:00Z",
        "quantidade_total": 200,
        "quantidade_em_uso": 150,
        "quantidade_disponivel": 50,
        "custo_unitario": 1590,
        "data_validade": "2028-06-01",
        "codigo_integracao": null,
        "nota_fiscal_id": 900
      }
    ],
    "total": 12,
    "limit": 50,
    "offset": 0
  }
}
```

**Status codes**: `200`, `401`, `403`, `404` (item não encontrado), `429`, `500`.

***

#### `GET /integracao/v1/estoque/item/{item_epi_id}/unitario`

Lista as unidades individuais rastreadas de um item (para itens com `controla_unitario = true`), com paginação e filtros.

**Requer módulo**: `modulo_epi`. **Restrição de unidade**: sim.

**Path params**: `item_epi_id` (integer, obrigatório). **Query params**:

| Parâmetro           | Tipo              | Descrição                                                                                         |
| ------------------- | ----------------- | ------------------------------------------------------------------------------------------------- |
| `limit`, `offset`   | integer           | Paginação padrão.                                                                                 |
| `estado`            | integer, opcional | `0`=Disponível, `1`=Em Uso, `2`=Manutenção, `3`=Inativo, `4`=Quebra, `5`=Perda, `6`=Higienização. |
| `centro_estoque_id` | integer, opcional | Filtra por centro de estoque — deve estar entre os centros vinculados às unidades permitidas da API Key. |

**Response `200`:**

```json
{
  "status": 200,
  "title": "OK",
  "data": {
    "dados": [
      {
        "id": 30001,
        "numero_serie": "SN-000123",
        "estado": 1,
        "funcionario_id": 987,
        "centro_estoque_id": 1,
        "item_epi_lote_id": 500,
        "usos": 3,
        "data_alocacao": "2026-05-10T08:00:00Z",
        "data_devolucao_prevista": "2026-11-06",
        "data_validade": "2028-06-01",
        "custo": 1590,
        "codigo_integracao": null
      }
    ],
    "total": 150,
    "limit": 50,
    "offset": 0
  }
}
```

{% hint style="info" %}
Desde a migração de estoque por Centro de Estoque, unitários são alocados a um `centro_estoque_id` — não mais diretamente a um `local_trabalho_id`. Se a API Key for restrita a unidades específicas, apenas unitários dos centros de estoque vinculados a essas unidades são retornados (resolução automática via `locais_trabalho_ids` → `centro_estoque_id`).
{% endhint %}

**Status codes**: `200`, `400` (`centro_estoque_id` fora das unidades permitidas para esta API Key), `401`, `403`, `404` (item não encontrado), `429`, `500`.

***

#### `GET /integracao/v1/estoque/item/{item_epi_id}/unitario/{unitario_id}`

Busca os dados de uma unidade individual específica.

**Requer módulo**: `modulo_epi`. **Restrição de unidade**: sim — retorna `404` se o unitário estiver em uma unidade não permitida.

**Path params**: `item_epi_id`, `unitario_id` (integers, obrigatórios).

**Response `200`**: mesmo formato de um item da listagem acima.

**Status codes**: `200`, `401`, `403`, `404`, `429`, `500`.

***

### Centro de Estoque

Centro de Estoque é a entidade que efetivamente guarda estoque (lotes e unitários) — cada local de trabalho (unidade) enxerga estoque através dos centros vinculados a ele, numa relação N:N (uma unidade pode puxar estoque de vários centros, e um centro pode abastecer várias unidades, ex: um Centro de Distribuição compartilhado). Um centro recém-criado não tem nenhuma unidade vinculada — use os endpoints de associar/desassociar abaixo para vinculá-lo.

{% hint style="info" %}
Um centro **inativado** não valida nem desfaz vínculos existentes com locais de trabalho — os vínculos continuam registrados, mas o centro deixa de aparecer nas listagens ativas (e, por consequência, nas consultas de estoque, compra e transferência).
{% endhint %}

#### `GET /integracao/v1/centro-estoque`

Lista os centros de estoque ativos da empresa autenticada.

**Requer módulo**: `modulo_epi`. **Restrição de unidade**: sim (filtro automático) — se a API Key for restrita a unidades, retorna apenas os centros vinculados a essas unidades.

**Response `200`:**

```json
{
  "status": 200,
  "title": "OK",
  "data": {
    "centros_estoque": [
      {
        "id": 1,
        "nome": "Centro de Distribuição São Paulo",
        "descricao": "Abastece as filiais da região sudeste",
        "endereco": null,
        "situacao": 0,
        "codigo_integracao": "CD-SP-01",
        "criado_em": "2026-07-28T10:00:00Z",
        "atualizado_em": "2026-07-28T10:00:00Z"
      }
    ],
    "total_centros_estoque": 1
  }
}
```

**Status codes**: `200`, `401`, `403`, `429`, `500`.

***

#### `POST /integracao/v1/centro-estoque`

Cria um novo centro de estoque para a empresa autenticada. O centro nasce sem nenhuma unidade vinculada.

**Requer módulo**: `modulo_epi`.

**Request body:**

```json
{
  "nome": "Centro de Distribuição São Paulo",
  "descricao": "Abastece as filiais da região sudeste",
  "endereco": "Av. Industrial, 1000 - São Paulo/SP",
  "codigo_integracao": "CD-SP-01"
}
```

| Campo               | Tipo             | Obrigatório | Descrição                                                     |
| -------------------- | ---------------- | ----------- | ---------------------------------------------------------------- |
| `nome`               | string (1-255)   | Sim         | Nome do centro de estoque.                                       |
| `descricao`          | string           | Não         | Descrição livre.                                                  |
| `endereco`           | string           | Não         | Endereço do centro.                                               |
| `codigo_integracao`  | string           | Não         | Código de referência no seu sistema — único por empresa.          |

**Response `201`**: mesmo formato de um item da listagem acima.

**Status codes**: `201`, `400` (payload inválido), `401`, `403`, `409` (`codigo_integracao` duplicado nesta empresa), `429`, `500`.

***

#### `GET /integracao/v1/centro-estoque/{centro_estoque_id}`

Detalha um centro de estoque específico.

**Requer módulo**: `modulo_epi`. **Restrição de unidade**: sim — `404` se o centro não estiver vinculado a uma unidade permitida.

**Path params**: `centro_estoque_id` (integer, obrigatório).

**Response `200`**: mesmo formato de um item da listagem acima.

**Status codes**: `200`, `401`, `403`, `404`, `429`, `500`.

***

#### `PATCH /integracao/v1/centro-estoque/{centro_estoque_id}`

Atualiza parcialmente um centro de estoque. Campos não enviados permanecem inalterados.

**Requer módulo**: `modulo_epi`. **Restrição de unidade**: sim.

**Path params**: `centro_estoque_id` (integer, obrigatório).

**Request body (todos os campos opcionais)**: mesmos campos do `POST`.

**Response `200`**: mesmo formato de um item da listagem acima, com os valores atualizados.

**Status codes**: `200`, `400`, `401`, `403`, `404`, `409` (`codigo_integracao` duplicado nesta empresa), `429`, `500`.

***

#### `DELETE /integracao/v1/centro-estoque/{centro_estoque_id}`

Inativa (soft delete) um centro de estoque.

**Requer módulo**: `modulo_epi`. **Restrição de unidade**: sim.

**Path params**: `centro_estoque_id` (integer, obrigatório).

**Response `204`**: sem corpo.

**Status codes**: `204`, `401`, `403`, `404`, `429`, `500`.

***

#### `POST /integracao/v1/centro-estoque/{centro_estoque_id}/local-trabalho`

Associa um local de trabalho (unidade) a um centro de estoque. **Operação idempotente** — associar um local já vinculado não é erro.

**Requer módulo**: `modulo_epi`. **Restrição de unidade**: sim — o centro e o `local_trabalho_id` informado precisam estar entre as unidades permitidas da chave.

**Path params**: `centro_estoque_id` (integer, obrigatório).

**Request body:**

```json
{
  "local_trabalho_id": 1
}
```

**Response `201`:**

```json
{
  "status": 201,
  "title": "Created",
  "data": {
    "centro_estoque_id": 1,
    "local_trabalho_id": 1
  }
}
```

**Status codes**: `201`, `400` (`local_trabalho_id` inválido, inativo, ou fora das unidades permitidas), `401`, `403`, `404` (centro de estoque não encontrado ou fora do escopo), `429`, `500`.

***

#### `GET /integracao/v1/centro-estoque/{centro_estoque_id}/local-trabalho`

Lista os locais de trabalho atualmente vinculados a um centro de estoque.

**Requer módulo**: `modulo_epi`. **Restrição de unidade**: sim.

**Path params**: `centro_estoque_id` (integer, obrigatório).

**Response `200`:**

```json
{
  "status": 200,
  "title": "OK",
  "data": {
    "locais_trabalho": [
      { "id": 1, "nome": "Filial São Paulo" }
    ],
    "total_locais_trabalho": 1
  }
}
```

**Status codes**: `200`, `401`, `403`, `404`, `429`, `500`.

***

#### `DELETE /integracao/v1/centro-estoque/{centro_estoque_id}/local-trabalho/{local_trabalho_id}`

Desassocia um local de trabalho de um centro de estoque.

**Requer módulo**: `modulo_epi`. **Restrição de unidade**: sim.

**Path params**: `centro_estoque_id`, `local_trabalho_id` (integers, obrigatórios).

**Response `204`**: sem corpo.

**Status codes**: `204`, `401`, `403`, `404` (centro de estoque, vínculo não encontrado, ou fora do escopo), `429`, `500`.

***

#### `GET /integracao/v1/local-trabalho/{local_trabalho_id}/centro-estoque`

Lista os centros de estoque atualmente vinculados a um local de trabalho.

**Requer módulo**: `modulo_epi`. **Restrição de unidade**: sim — `400` se `local_trabalho_id` estiver fora das unidades permitidas da chave.

**Path params**: `local_trabalho_id` (integer, obrigatório).

**Response `200`**: mesmo formato da listagem de `GET /centro-estoque` acima.

**Status codes**: `200`, `400`, `401`, `403`, `404` (local de trabalho não encontrado para esta empresa), `429`, `500`.

***

### Certificados de Aprovação (CA)

#### `GET /integracao/v1/ca/{numero_ca}`

Consulta um Certificado de Aprovação (CA) na base do Ministério do Trabalho e informa se ele está válido. Útil para validar o CA antes de cadastrar um item.

**Requer módulo**: `modulo_epi`.

**Path params**: `numero_ca` (string, obrigatório).

**Response `200`:**

```json
{
  "status": 200,
  "title": "OK",
  "data": {
    "registro_ca": "12345",
    "valido": true,
    "situacao": "VALIDO",
    "data_validade": "2028-06-01",
    "nome_equipamento": "Protetor Auricular Tipo Concha",
    "descricao_equipamento": "Protetor auricular tipo concha, atenuação de 25dB",
    "marca_ca": "3M",
    "referencia": "1425",
    "cor": "Verde",
    "cnpj_fabricante": "00000000000191",
    "razao_social_fabricante": "3M do Brasil Ltda",
    "norma": "NBR NM 300-6"
  }
}
```

{% hint style="warning" %}
Os nomes de campo reais são `registro_ca` (não `numero_ca`), `nome_equipamento`/`descricao_equipamento` (não `descricao_produto`) e `razao_social_fabricante` (não `empresa_fabricante`).
{% endhint %}

**Status codes**: `200`, `401`, `403`, `404` (CA não encontrado na base), `429`, `500`, `503` (serviço de CA indisponível).

***

### Solicitações

Quatro tipos de solicitação são expostos para consulta: **EPI** (retirada/entrega/devolução por colaborador), **compra** (reposição de estoque), **transferência** (entre unidades) e **parceiro** (pedidos de fornecedores/prestadores para a empresa). Todos são **somente leitura** nesta API — criação e aprovação continuam sendo feitas pelo painel GNRx.

#### `GET /integracao/v1/solicitacao/epi`

Lista as solicitações de EPI, paginado, com filtros.

**Requer módulo**: `modulo_epi`. **Restrição de unidade**: sim (filtro automático).

**Query params**: `limit`, `offset`, `situacao` (string, opcional, ex: `"pendente"`, `"aprovada"`, `"rejeitada"`), `data_inicio` (datetime ISO 8601, opcional), `data_fim` (datetime ISO 8601, opcional).

**Response `200`:**

```json
{
  "status": 200,
  "title": "OK",
  "data": {
    "dados": [
      {
        "id": 7001,
        "solicitacao_id": 6500,
        "epi_id": "EPI_001",
        "local_trabalho_id": 1,
        "funcionario_id": 987,
        "solicitado_em": "2026-06-30T14:00:00Z",
        "entregue_em": null,
        "entregue": false,
        "cancelado": false,
        "numero_solicitacao_epi_empresa": 7001,
        "situacao": "pendente"
      }
    ],
    "total": 42,
    "limit": 50,
    "offset": 0
  }
}
```

{% hint style="info" %}
`id` é o ID do item individual dentro da solicitação; `solicitacao_id` é o ID da solicitação-pai (pode agrupar múltiplos itens). `epi_id` referencia o tipo de item (ver [Tipos de Item](api-integracao.md#tipos-de-item)), não o item de estoque (`item_epi_id`).
{% endhint %}

**Status codes**: `200`, `401`, `403`, `429`, `500`.

***

#### `GET /integracao/v1/solicitacao/epi/{id}`

Detalha uma solicitação de EPI específica.

**Restrição de unidade**: sim — `404` se fora do escopo.

**Path params**: `id` (integer, obrigatório).

**Response `200`**: mesmo formato de um item da listagem acima, com detalhamento completo.

**Status codes**: `200`, `401`, `403`, `404`, `429`, `500`.

***

#### `GET /integracao/v1/solicitacao/compra`

Lista as solicitações de compra de itens para reposição de estoque.

**Requer módulo**: `modulo_epi`. **Restrição de unidade**: sim — filtro automático: retorna solicitações cujo centro de estoque vinculado corresponde a um dos centros vinculados às unidades permitidas da API Key.

**Query params**: `limit`, `offset`, `status` (integer, opcional: `0`=pendente, `1`=aprovada, `2`=rejeitada, `3`=cancelada, `4`=processada).

**Response `200`:**

```json
{
  "status": 200,
  "title": "OK",
  "data": {
    "dados": [
      {
        "id": 8001,
        "centro_estoque_id": 1,
        "numero_solicitacao": 8001,
        "status": 0,
        "observacoes": null,
        "justificativa": "Reposição de estoque mínimo",
        "criado_em": "2026-06-28T09:00:00Z",
        "atualizado_em": "2026-06-28T09:00:00Z"
      }
    ],
    "total": 15,
    "limit": 50,
    "offset": 0
  }
}
```

{% hint style="warning" %}
Não existe query param `local_trabalho_id` nem campos `item_epi_id`/`quantidade`/`data_solicitacao` neste recurso — a solicitação de compra é um cabeçalho vinculado a um `centro_estoque_id`; os itens/quantidades solicitados não são expostos por esta API.
{% endhint %}

**Status codes**: `200`, `401`, `403`, `429`, `500`.

***

#### `GET /integracao/v1/solicitacao/compra/{id}`

Detalha uma solicitação de compra específica.

**Path params**: `id` (integer, obrigatório).

**Status codes**: `200`, `401`, `403`, `404`, `429`, `500`.

***

#### `GET /integracao/v1/solicitacao/transferencia`

Lista as solicitações de transferência de itens entre unidades.

**Requer módulo**: `modulo_epi`. **Restrição de unidade**: sim — retorna solicitações em que a unidade permitida é origem **ou** destino.

**Query params**: `limit`, `offset`, `status` (integer, opcional).

**Response `200`:**

```json
{
  "status": 200,
  "title": "OK",
  "data": {
    "dados": [
      {
        "id": 9001,
        "centro_estoque_id": 1,
        "centro_estoque_destino_id": 2,
        "numero_solicitacao": 9001,
        "status": 0,
        "observacoes": null,
        "justificativa": "Reposição da filial 2",
        "criado_em": "2026-06-29T11:00:00Z",
        "atualizado_em": "2026-06-29T11:00:00Z"
      }
    ],
    "total": 6,
    "limit": 50,
    "offset": 0
  }
}
```

{% hint style="warning" %}
Os campos de unidade são `centro_estoque_id` (origem) e `centro_estoque_destino_id` — não `origem_local_trabalho_id`/`destino_local_trabalho_id`. Não há campos `item_epi_id`/`quantidade`/`data_solicitacao` neste recurso.
{% endhint %}

**Status codes**: `200`, `401`, `403`, `429`, `500`.

***

#### `GET /integracao/v1/solicitacao/transferencia/{id}`

Detalha uma solicitação de transferência específica.

**Path params**: `id` (integer, obrigatório).

**Status codes**: `200`, `401`, `403`, `404`, `429`, `500`.

***

#### `GET /integracao/v1/solicitacao/parceiro`

Lista as solicitações feitas por parceiros (fornecedores/prestadores) para a empresa. **Não tem relação com unidade de trabalho.**

**Requer módulo**: `modulo_epi`.

**Query params**: `limit`, `offset`, `status` (integer, opcional: `0`=pendente, `1`=aprovada, `2`=rejeitada).

**Response `200`:**

```json
{
  "status": 200,
  "title": "OK",
  "data": {
    "dados": [
      {
        "id": 3001,
        "parceiro_id": 22,
        "numero_solicitacao": 3001,
        "status": 0,
        "observacoes": "Solicitação de reposição de EPIs para equipe terceirizada",
        "solicitado_em": "2026-06-27T15:00:00Z",
        "criado_em": "2026-06-27T15:00:00Z",
        "atualizado_em": "2026-06-27T15:00:00Z"
      }
    ],
    "total": 3,
    "limit": 50,
    "offset": 0
  }
}
```

{% hint style="warning" %}
Os campos reais são `observacoes` (não `descricao`) e `solicitado_em` (não `data_solicitacao`).
{% endhint %}

**Status codes**: `200`, `401`, `403`, `429`, `500`.

***

#### `GET /integracao/v1/solicitacao/parceiro/{id}`

Detalha uma solicitação de parceiro específica.

**Path params**: `id` (integer, obrigatório).

**Status codes**: `200`, `401`, `403`, `404`, `429`, `500`.

***

## Fluxos de exemplo (cookbook)

### Onboarding de um novo funcionário

```bash
# 1. Criar o funcionário já vinculado a local, setor e cargos
curl -X POST https://<dominio>/integracao/v1/funcionario \
  -H "X-Gnrx-Api-Key: gnrx_sua_chave" \
  -H "Content-Type: application/json" \
  -d '{
        "nome": "Maria Souza",
        "cpf": "98765432100",
        "senha": "654321",
        "codigo_integracao": "EMP-002",
        "locais_trabalho": [
          { "local_trabalho_id": 1, "setores": [ { "setor_id": 5, "cargos": [10] } ] }
        ]
      }'

# 2. Se precisar desativar depois, localize pelo código do seu sistema (sem guardar o ID interno):
curl -X DELETE https://<dominio>/integracao/v1/funcionario/codigo/EMP-002 \
  -H "X-Gnrx-Api-Key: gnrx_sua_chave"
```

### Montar um GHE completo do zero

```bash
# 1. Criar o GHE
curl -X POST https://<dominio>/integracao/v1/ghe \
  -H "X-Gnrx-Api-Key: gnrx_sua_chave" -H "Content-Type: application/json" \
  -d '{ "nome": "GHE Almoxarifado", "local_trabalho_id": 1 }'
# → retorna { "data": { "id": 51, ... } }

# 2. Vincular um risco ocupacional já existente ao GHE
curl -X POST https://<dominio>/integracao/v1/ghe/51/riscos \
  -H "X-Gnrx-Api-Key: gnrx_sua_chave" -H "Content-Type: application/json" \
  -d '{ "risco_ocupacional_id": 12 }'

# 3. Vincular um item (EPI) obrigatório a esse risco, dentro do GHE
curl -X POST https://<dominio>/integracao/v1/ghe/51/riscos/12/epis \
  -H "X-Gnrx-Api-Key: gnrx_sua_chave" -H "Content-Type: application/json" \
  -d '{ "epi_id": "EPI_001", "obrigatorio": true }'

# 4. Conferir o resultado completo
curl https://<dominio>/integracao/v1/ghe/51 -H "X-Gnrx-Api-Key: gnrx_sua_chave"
```

### Sincronizar estoque com paginação

```bash
# Página 1
curl "https://<dominio>/integracao/v1/estoque/item?limit=100&offset=0" \
  -H "X-Gnrx-Api-Key: gnrx_sua_chave"

# Enquanto offset + limit < total retornado, siga incrementando:
curl "https://<dominio>/integracao/v1/estoque/item?limit=100&offset=100" \
  -H "X-Gnrx-Api-Key: gnrx_sua_chave"

# Para um item específico, ver as unidades individuais disponíveis em um centro de estoque:
curl "https://<dominio>/integracao/v1/estoque/item/100/unitario?estado=0&centro_estoque_id=1" \
  -H "X-Gnrx-Api-Key: gnrx_sua_chave"
```

### Consultar solicitações de EPI pendentes de um período

```bash
curl "https://<dominio>/integracao/v1/solicitacao/epi?situacao=pendente&data_inicio=2026-06-01T00:00:00Z&data_fim=2026-06-30T23:59:59Z&limit=100" \
  -H "X-Gnrx-Api-Key: gnrx_sua_chave"
```

## Referência rápida de endpoints

| Método | Path                                                               | Grupo                     |
| ------ | ------------------------------------------------------------------ | ------------------------- |
| GET    | `/integracao/v1/ping`                                              | Autenticação              |
| POST   | `/integracao/v1/funcionario`                                       | Funcionários              |
| DELETE | `/integracao/v1/funcionario/{funcionario_id}`                      | Funcionários              |
| DELETE | `/integracao/v1/funcionario/codigo/{codigo_integracao}`            | Funcionários              |
| PATCH  | `/integracao/v1/funcionario/{funcionario_id}/reativar`             | Funcionários              |
| PATCH  | `/integracao/v1/funcionario/codigo/{codigo_integracao}/reativar`   | Funcionários              |
| GET    | `/integracao/v1/local-trabalho`                                    | Locais de Trabalho        |
| GET    | `/integracao/v1/local-trabalho/{local_trabalho_id}/centro-estoque` | Centro de Estoque         |
| GET    | `/integracao/v1/centro-estoque`                                    | Centro de Estoque         |
| POST   | `/integracao/v1/centro-estoque`                                    | Centro de Estoque         |
| GET    | `/integracao/v1/centro-estoque/{centro_estoque_id}`                | Centro de Estoque         |
| PATCH  | `/integracao/v1/centro-estoque/{centro_estoque_id}`                | Centro de Estoque         |
| DELETE | `/integracao/v1/centro-estoque/{centro_estoque_id}`                | Centro de Estoque         |
| POST   | `/integracao/v1/centro-estoque/{centro_estoque_id}/local-trabalho` | Centro de Estoque         |
| GET    | `/integracao/v1/centro-estoque/{centro_estoque_id}/local-trabalho` | Centro de Estoque         |
| DELETE | `/integracao/v1/centro-estoque/{centro_estoque_id}/local-trabalho/{local_trabalho_id}` | Centro de Estoque |
| GET    | `/integracao/v1/ghe`                                               | GHEs                      |
| GET    | `/integracao/v1/ghe/{ghe_id}`                                      | GHEs                      |
| POST   | `/integracao/v1/ghe`                                               | GHEs                      |
| PATCH  | `/integracao/v1/ghe/{ghe_id}`                                      | GHEs                      |
| POST   | `/integracao/v1/ghe/{ghe_id}/riscos`                               | GHEs                      |
| DELETE | `/integracao/v1/ghe/{ghe_id}/riscos/{risco_id}`                    | GHEs                      |
| POST   | `/integracao/v1/ghe/{ghe_id}/riscos/{risco_id}/epis`               | GHEs                      |
| DELETE | `/integracao/v1/ghe/{ghe_id}/riscos/{risco_id}/epis/{epi_id}`      | GHEs                      |
| GET    | `/integracao/v1/setor`                                             | Setores                   |
| POST   | `/integracao/v1/setor`                                             | Setores                   |
| PATCH  | `/integracao/v1/setor/{setor_id}`                                  | Setores                   |
| DELETE | `/integracao/v1/setor/{setor_id}`                                  | Setores                   |
| GET    | `/integracao/v1/cargo`                                             | Cargos                    |
| POST   | `/integracao/v1/cargo`                                             | Cargos                    |
| PATCH  | `/integracao/v1/cargo/{cargo_id}`                                  | Cargos                    |
| DELETE | `/integracao/v1/cargo/{cargo_id}`                                  | Cargos                    |
| GET    | `/integracao/v1/risco`                                             | Riscos Ocupacionais       |
| POST   | `/integracao/v1/risco`                                             | Riscos Ocupacionais       |
| PATCH  | `/integracao/v1/risco/{risco_id}`                                  | Riscos Ocupacionais       |
| DELETE | `/integracao/v1/risco/{risco_id}`                                  | Riscos Ocupacionais       |
| GET    | `/integracao/v1/tipo-item`                                         | Tipos de Item             |
| POST   | `/integracao/v1/tipo-item`                                         | Tipos de Item             |
| GET    | `/integracao/v1/categoria-produto`                                 | Categorias de Produto     |
| POST   | `/integracao/v1/categoria-produto`                                 | Categorias de Produto     |
| GET    | `/integracao/v1/estoque/item`                                      | Estoque                   |
| POST   | `/integracao/v1/estoque/item`                                      | Estoque                   |
| GET    | `/integracao/v1/estoque/item/{item_epi_id}/lote`                   | Estoque                   |
| GET    | `/integracao/v1/estoque/item/{item_epi_id}/unitario`               | Estoque                   |
| GET    | `/integracao/v1/estoque/item/{item_epi_id}/unitario/{unitario_id}` | Estoque                   |
| GET    | `/integracao/v1/ca/{numero_ca}`                                    | Certificados de Aprovação |
| GET    | `/integracao/v1/solicitacao/epi`                                   | Solicitações              |
| GET    | `/integracao/v1/solicitacao/epi/{id}`                              | Solicitações              |
| GET    | `/integracao/v1/solicitacao/compra`                                | Solicitações              |
| GET    | `/integracao/v1/solicitacao/compra/{id}`                           | Solicitações              |
| GET    | `/integracao/v1/solicitacao/transferencia`                         | Solicitações              |
| GET    | `/integracao/v1/solicitacao/transferencia/{id}`                    | Solicitações              |
| GET    | `/integracao/v1/solicitacao/parceiro`                              | Solicitações              |
| GET    | `/integracao/v1/solicitacao/parceiro/{id}`                         | Solicitações              |

**Total: 54 endpoints.**
