# Motivos de Solicitação

Esta página explica como configurar e gerenciar os motivos de solicitação de EPIs no Sistema GNRX.

## Visão Geral

Os motivos de solicitação são categorias predefinidas que indicam a razão pela qual um EPI está sendo solicitado para um colaborador. Estas categorias são essenciais para:

- Padronizar processos de solicitação
- Gerar estatísticas precisas sobre consumo
- Identificar padrões que possam indicar problemas
- Estabelecer fluxos específicos para cada tipo de solicitação

## Acessando a Configuração de Motivos de Solicitação

1. No menu lateral, acesse **Configurações Gerais**
2. Selecione **Motivos**
3. Clique na aba **Motivos de Solicitação**

![Acesso a Motivos de Solicitação](../../../assets/images/acesso-motivos-solicitacao.png)

## Motivos Padrão do Sistema

O Sistema GNRX vem pré-configurado com os seguintes motivos de solicitação:

| Motivo | Sigla | Descrição | Comportamento |
|--------|-------|-----------|---------------|
| Primeira Entrega | PRIM | Primeira vez que o colaborador recebe este EPI | Não exige devolução de item anterior |
| Substituição por Desgaste | DESG | EPI atual apresenta desgaste natural pelo uso | Exige devolução do item anterior |
| Substituição por Perda | PERD | Colaborador perdeu ou extraviou o EPI | Não exige devolução, mas registra ocorrência |
| Substituição por Quebra | QEBR | EPI danificado ou quebrado | Exige devolução do item danificado |
| Substituição por Validade Vencida | VENC | EPI com data de validade expirada | Exige devolução do item vencido |
| Outros | OUTR | Situações não previstas nas categorias anteriores | Exige descrição adicional |

## Gerenciando Motivos de Solicitação

### Adicionando um Novo Motivo

![Adicionar Motivo](../../../assets/images/adicionar-motivo-solicitacao.png)

1. Clique no botão **Adicionar Motivo**
2. Preencha o formulário com:
   - **Motivo**: Nome descritivo (ex: "Mudança de Função")
   - **Sigla**: Abreviação de 2 a 4 letras (ex: "FUNC")
   - **Descrição**: Detalhamento do motivo (opcional)
   - **Comportamento**:
     - Exige devolução: Se marcado, o sistema solicitará a devolução do item anterior
     - Registra perda/dano: Se marcado, o sistema registrará ocorrência associada ao colaborador
     - Exige aprovação: Se marcado, solicitações com este motivo exigirão aprovação especial
3. Clique em **Salvar**

### Editando um Motivo Existente

1. Localize o motivo na lista
2. Clique no ícone de **Editar** (símbolo de lápis)
3. Faça as alterações necessárias
4. Clique em **Salvar**

> **Nota:** A edição de motivos afetará apenas novas solicitações. Solicitações já registradas manterão o motivo original.

### Desativando um Motivo

1. Localize o motivo na lista
2. Clique no ícone de **Desativar** (símbolo de proibido)
3. Confirme a desativação no diálogo exibido

> **Importante:** Motivos desativados não estarão mais disponíveis para novas solicitações, mas permanecerão visíveis em registros históricos.

## Impacto nos Fluxos de Trabalho

A configuração de motivos impacta diretamente:

1. **Tela de Solicitação**: Define as opções disponíveis no momento da criação de uma solicitação
2. **Fluxo de Entrega**: Determina se será exigida devolução de item anterior
3. **Relatórios**: Permite análises estatísticas por tipo de motivo
4. **Alertas**: Motivos como perda ou quebra frequente podem gerar alertas automáticos

## Recomendações e Boas Práticas

- Mantenha a lista de motivos concisa e clara para facilitar a seleção pelos usuários
- Utilize motivos específicos para situações recorrentes na sua organização
- Considere criar motivos relacionados a particularidades do seu setor ou operação
- Avalie periodicamente a frequência de cada motivo para identificar oportunidades de melhoria
- Padronize a nomenclatura e siglas para facilitar relatórios e análises
- Documente internamente o significado e critérios para uso de cada motivo personalizado