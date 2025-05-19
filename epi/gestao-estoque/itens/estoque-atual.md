# Estoque Atual

Esta página explica como gerar e interpretar relatórios de estoque atual no Sistema GNRX Gestão de EPI.

## Visão Geral

O relatório de Estoque Atual fornece uma visão completa e instantânea da situação do inventário de EPIs, permitindo visualizar quantidades disponíveis, itens em uso, níveis de estoque por local e status detalhado de cada unidade física de equipamento.

![Relatório de Estoque Atual](../../../assets/images/relatorio-estoque-atual.png)

## Acessando o Relatório

Para acessar o relatório de estoque atual:

1. No menu lateral, clique em **Inventário**
2. Selecione **Inventário de Items**
3. Clique no botão **Exportar PDF** no canto superior direito
4. Selecione a opção **Completo** para o relatório mais detalhado

Alternativamente, você pode acessar informações de estoque detalhadas para um item específico:

1. Clique no item desejado na lista para abrir seus detalhes
2. Navegue entre as abas **Informações Item**, **Inventário Detalhado** e **Lotes**

## Informações Disponíveis

O relatório de estoque atual apresenta:

### Visão Consolidada
- **Total de itens cadastrados**: Quantidade de diferentes tipos de EPIs
- **Total em estoque**: Soma de todas as unidades disponíveis
- **Total em uso**: Quantidade de equipamentos atualmente alocados a colaboradores
- **Total por situação**: Distribuição por status (disponível, em uso, perda, quebra)

### Por Item de EPI
- **Estoque total**: Número total de unidades de cada tipo de EPI
- **Tempo de troca**: Período de substituição recomendado
- **Validade**: Data limite de utilização baseada no CA
- **Distribuição por variante**: Quantidades por tamanho, cor ou outras características

### Inventário Detalhado
- **Número de série**: Identificador único de cada unidade física
- **Estado**: Status atual (disponível, em uso, inativo, perda, quebra)
- **Validade**: Data de vencimento específica daquela unidade
- **Número de usos**: Quantas vezes o item foi utilizado
- **Colaborador**: Pessoa atualmente usando o equipamento (quando aplicável)
- **Unidade**: Localização física do equipamento
- **Histórico**: Datas de alocação e previsão de devolução

## Filtragem e Personalização

O relatório pode ser filtrado por:

- **Unidade**: Para visualizar apenas o estoque de um local específico
- **Tipo de EPI**: Para focar em categorias específicas de equipamentos
- **Status**: Para visualizar apenas itens disponíveis, em uso, etc.
- **Período de validade**: Para identificar itens próximos ao vencimento

## Formato de Exportação

O sistema permite exportar o relatório em diferentes formatos:

- **Resumido**: Visão condensada apenas com totais por item
- **Variações**: Inclui detalhamento por variantes de cada item
- **Completo**: Relatório detalhado com todas as informações disponíveis

A exportação gera um arquivo PDF estruturado que pode ser salvo, impresso ou compartilhado.

## Uso Prático do Relatório

O relatório de Estoque Atual é útil para:

- **Planejamento de compras**: Identificar itens com baixo estoque
- **Controle de validade**: Verificar equipamentos próximos ao vencimento
- **Auditoria interna**: Conferir a distribuição e uso dos EPIs
- **Conformidade legal**: Documentar a disponibilidade de equipamentos certificados
- **Análise financeira**: Avaliar o valor do inventário atual

## Interpretação dos Status

O relatório utiliza os seguintes códigos de status:

- **Disponível**: Itens em estoque prontos para uso
- **Em Uso**: Equipamentos atualmente alocados a colaboradores
- **Inativo**: Itens desativados ou fora de conformidade
- **Perda**: Equipamentos registrados como perdidos
- **Quebra**: Itens danificados e fora de uso

## Tomada de Decisão Baseada em Dados

Utilize o relatório para decisões estratégicas:

1. **Nível crítico de estoque**: Identifique itens abaixo do mínimo recomendado
2. **Renovação de CA**: Verifique equipamentos com certificados próximos do vencimento
3. **Análise de uso**: Avalie quais EPIs têm maior rotatividade
4. **Otimização de recursos**: Redistribua equipamentos entre unidades conforme necessidade

## Próximos Passos

Com base no relatório de Estoque Atual, você pode:

- [Adicionar novos lotes](../lotes/adicionar-lote.md) para itens com estoque baixo
- Gerar [relatórios de movimentação](./movimentacao-estoque.md) para análise temporal
- Verificar [itens por validade](./items-por-validade.md) para planejamento de substituições
- Analisar a [previsão de consumo](./previsao-consumo.md) para compras futuras

---

*Última atualização: 18 de Maio de 2025*