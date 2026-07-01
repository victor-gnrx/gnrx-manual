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
| `codigo_integracao` | string              | Não         | Código do funcionário no seu sistema de origem, usado para futuras operações (inativar/reativar por código). |
| `locais_trabalho`   | array               | Sim         | Locais de trabalho, setores e cargos aos quais o funcionário é associado na criação.                         |

**Response `201`:**

```json
{
  "status": 201,
  "title": "Created",
  "data": {
    "id": 987,
    "nome": "João da Silva",
    "cpf": "12345678901",
    "codigo_integracao": "EMP-001",
    "situacao": 0,
    "criado_em": "2026-07-01T12:00:00Z"
  }
}
```

**Status codes**: `201`, `400`, `401`, `500`.

***

#### `DELETE /integracao/v1/funcionario/{funcionario_id}`

Inativa um funcionário pelo ID interno. Se o funcionário possuir itens ativos em seu nome, retorna `409` pedindo confirmação explícita. Reconhecimentos faciais associados são removidos automaticamente.

**Path params**: `funcionario_id` (integer, obrigatório).

**Request body (opcional, para confirmar mesmo com itens ativos):**

```json
{
  "confirmacoes": ["possui_itens_ativos"]
}
```

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
    "locais": [
      {
        "id": 1,
        "nome": "Filial São Paulo",
        "ativo": true,
        "contagem_funcionarios": 150,
        "contagem_ghes": 8
      }
    ]
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
    ]
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
    ]
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
    "cargos": [{ "id": 10, "nome": "operador de produção", "situacao": 0 }]
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
    ]
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
        "nome": "Protetor Auricular",
        "descricao": "Protetores auriculares tipo concha ou plug",
        "categoria_produto_id": 3,
        "categoria_nome": "Proteção Auditiva",
        "situacao": 0
      }
    ]
  }
}
```

**Status codes**: `200`, `401`, `403`, `429`, `500`.

***

#### `POST /integracao/v1/tipo-item`

Cria um novo tipo de item, vinculado a uma categoria de produto já cadastrada.

**Requer módulo**: `modulo_epi`.

**Request body:**

```json
{
  "nome": "Luva de Raspa",
  "descricao": "Luvas de proteção para manuseio de materiais abrasivos",
  "categoria_produto_id": 5,
  "codigo_integracao": "TIPO-LUVA-01"
}
```

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
        "situacao": 0
      }
    ]
  }
}
```

**Status codes**: `200`, `401`, `403`, `429`, `500`.

***

#### `POST /integracao/v1/categoria-produto`

Cria uma nova categoria de produto.

**Requer módulo**: `modulo_epi`.

**Request body:**

```json
{
  "nome": "Uniformes",
  "descricao": "Uniformes e vestimentas de trabalho"
}
```

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
        "epi_id": "EPI_001",
        "tipo_epi_nome": "Protetor Auricular",
        "numero_ca": "12345",
        "fabricante_id": 7,
        "custo": 1590,
        "tempo_troca_dias": 180,
        "controla_unitario": true,
        "sem_devolucao": false,
        "unidade_medida": "un",
        "casas_decimais": 0,
        "situacao": 0
      }
    ],
    "total": 340,
    "limit": 50,
    "offset": 0
  }
}
```

{% hint style="info" %}
`custo` está em **centavos** (1590 = R$ 15,90).
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
| `numero_ca`         | string (máx. 20) | Não                  | Número do Certificado de Aprovação, se aplicável.                                        |
| `fabricante_id`     | integer          | Não                  | ID do fabricante.                                                                        |
| `custo`             | integer          | Não                  | Custo unitário em centavos.                                                              |
| `tempo_troca_dias`  | integer          | Não                  | Período padrão de troca, em dias.                                                        |
| `controla_unitario` | boolean          | Não (padrão `true`)  | Se cada unidade é rastreada individualmente por número de série.                         |
| `sem_devolucao`     | boolean          | Não (padrão `false`) | Se o item não é passível de devolução após entrega.                                      |
| `unidade_medida`    | string           | Não (padrão `"un"`)  | Unidade de medida (`un`, `kg`, `L`, `m`, etc.).                                          |
| `casas_decimais`    | integer          | Não (padrão `0`)     | Casas decimais para itens medidos em fração (ex: metros, litros).                        |
| `codigo_integracao` | string           | Não                  | Código de referência no seu sistema.                                                     |

**Response `201`**: mesmo formato de um item da listagem acima.

**Status codes**: `201`, `400` (payload inválido ou `epi_id` não encontrado), `401`, `403`, `409` (CA duplicado nesta empresa), `429`, `500`.

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
| `local_trabalho_id` | integer, opcional | Filtra por unidade — deve estar entre as unidades permitidas da API Key.                          |

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
        "local_trabalho_id": 1,
        "funcionario_id": 987,
        "usos": 3,
        "data_alocacao": "2026-05-10T08:00:00Z",
        "data_devolucao_prevista": "2026-11-06",
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

**Status codes**: `200`, `400` (`local_trabalho_id` fora das unidades permitidas), `401`, `403`, `404` (item não encontrado), `429`, `500`.

***

#### `GET /integracao/v1/estoque/item/{item_epi_id}/unitario/{unitario_id}`

Busca os dados de uma unidade individual específica.

**Requer módulo**: `modulo_epi`. **Restrição de unidade**: sim — retorna `404` se o unitário estiver em uma unidade não permitida.

**Path params**: `item_epi_id`, `unitario_id` (integers, obrigatórios).

**Response `200`**: mesmo formato de um item da listagem acima.

**Status codes**: `200`, `401`, `403`, `404`, `429`, `500`.

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
    "numero_ca": "12345",
    "valido": true,
    "descricao_produto": "Protetor Auricular Tipo Concha",
    "empresa_fabricante": "3M do Brasil"
  }
}
```

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
        "funcionario_id": 987,
        "item_epi_id": 100,
        "quantidade": 1,
        "situacao": "pendente",
        "data_solicitacao": "2026-06-30T14:00:00Z"
      }
    ],
    "total": 42,
    "limit": 50,
    "offset": 0
  }
}
```

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

**Requer módulo**: `modulo_epi`. **Restrição de unidade**: sim (validação se `local_trabalho_id` for informado).

**Query params**: `limit`, `offset`, `status` (integer, opcional: `0`=pendente, `1`=aprovada, `2`=rejeitada, `3`=cancelada, `4`=processada), `local_trabalho_id` (integer, opcional).

**Response `200`:**

```json
{
  "status": 200,
  "title": "OK",
  "data": {
    "dados": [
      {
        "id": 8001,
        "item_epi_id": 100,
        "quantidade": 200,
        "status": 0,
        "local_trabalho_id": 1,
        "data_solicitacao": "2026-06-28T09:00:00Z"
      }
    ],
    "total": 15,
    "limit": 50,
    "offset": 0
  }
}
```

**Status codes**: `200`, `400` (`local_trabalho_id` fora das unidades permitidas), `401`, `403`, `429`, `500`.

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
        "item_epi_id": 100,
        "quantidade": 30,
        "origem_local_trabalho_id": 1,
        "destino_local_trabalho_id": 2,
        "status": 0,
        "data_solicitacao": "2026-06-29T11:00:00Z"
      }
    ],
    "total": 6,
    "limit": 50,
    "offset": 0
  }
}
```

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
        "descricao": "Solicitação de reposição de EPIs para equipe terceirizada",
        "status": 0,
        "data_solicitacao": "2026-06-27T15:00:00Z"
      }
    ],
    "total": 3,
    "limit": 50,
    "offset": 0
  }
}
```

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

# Para um item específico, ver as unidades individuais disponíveis em uma unidade:
curl "https://<dominio>/integracao/v1/estoque/item/100/unitario?estado=0&local_trabalho_id=1" \
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

**Total: 45 endpoints.**
