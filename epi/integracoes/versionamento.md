---
description: Como a API de Integração GNRx versiona mudanças, mantendo todas as versões publicadas disponíveis
icon: code-compare
---

# Política de Versionamento

{% hint style="info" %}
Aplica-se à API pública de integração (`/integracao/v1/` e ambiente de sandbox `/integracao/sandbox/v1/`), consumida por sistemas externos (ERPs, sistemas de RH, etc.).
{% endhint %}

## Esquema de versionamento

A API é versionada por **path (URL)**:

```
/integracao/v1/...
/integracao/v2/...   (futura, quando necessário)
```

A versão atual estável é `v1`. Uma nova versão major (`v2`) só é criada quando há mudança que quebra compatibilidade com o que já está publicado. Não há versionamento por header (`Accept-Version`) nem por query string — o path é a única fonte da verdade sobre qual versão está sendo usada.

## O que é mudança compatível (não gera nova versão)

As mudanças abaixo são consideradas **aditivas** e podem ser lançadas a qualquer momento dentro da mesma versão (`v1`), sem aviso prévio obrigatório:

- Novos endpoints.
- Novos campos **opcionais** em request ou response.
- Novos valores possíveis em enums existentes (ex: novo status), desde que os valores antigos continuem válidos.
- Novos filtros/parâmetros de query opcionais em endpoints existentes.
- Melhorias de performance, mensagens de erro mais descritivas, novos eventos de webhook.

Clientes integrados devem seguir a prática de **ignorar campos desconhecidos** na resposta, para não quebrar com essas adições.

## O que é mudança que quebra compatibilidade (exige nova versão)

As mudanças abaixo **nunca** são feitas dentro de uma versão existente — exigem uma nova versão major (`v2`, etc.):

- Remoção ou renomeação de um campo em request/response.
- Mudança de tipo de um campo (ex: string → integer).
- Mudança de comportamento de validação que torna uma requisição antes válida em inválida.
- Remoção de um endpoint.
- Mudança no formato do envelope de resposta ou de erro.
- Mudança de regra de negócio que altere o resultado de uma operação já documentada.

## Ciclo de vida das versões

- Como esta é uma API aberta, usada por integrações de terceiros, uma versão publicada **nunca é desativada**: `v1` continua disponível e funcionando normalmente mesmo depois do lançamento de uma `v2`.
- O lançamento de uma nova versão é anunciado por e-mail aos responsáveis técnicos cadastrados de cada API Key, além de publicado no changelog (ver [Changelog](#changelog)).
- Correções de segurança são aplicadas a todas as versões em uso, independentemente de há quanto tempo foram lançadas.
- Migrar para a versão mais nova dá acesso a novidades, mas nunca é obrigatório — integrações já existentes continuam funcionando sem nenhuma alteração.

## Ambiente de sandbox

Antes de uma mudança de versão chegar à produção, ela é validada no ambiente de sandbox, disponível no mesmo path da API de produção com o prefixo `sandbox` antes da versão:

```
/integracao/sandbox/v1/...
```

O sandbox espelha o comportamento da API de produção e usa uma **API Key de teste dedicada** (não compartilhada com a chave de produção), permitindo testar integrações e validar novas versões sem impacto em dados reais.

## Referências

- Documentação da API: `https://manual.gnrx.com.br/gnrx-gestao-de-epis-manual/integracoes/api-integracao`
- Swagger/OpenAPI interativo: `https://api.gnrx.com.br/integracao/docs/`
- Webhooks: `https://manual.gnrx.com.br/gnrx-gestao-de-epis-manual/integracoes/webhooks`
