# Visão Geral

## Introdução

O módulo de Lotes permite gerenciar a entrada e o controle de estoque dos Equipamentos de Proteção Individual (EPIs) no Sistema GNRX. Utilizando uma abordagem baseada em lotes, o sistema proporciona rastreabilidade completa, controle de validade e gerenciamento detalhado de cada unidade física de equipamento.

<figure><img src="../../.gitbook/assets/image (36).png" alt=""><figcaption><p>Visão Geral dos Lotes</p></figcaption></figure>

## Função e Importância

O gerenciamento por lotes permite:

* Rastrear cada unidade de EPI individualmente
* Controlar datas de validade específicas por lote
* Monitorar custos e valores de inventário
* Distribuir os equipamentos entre diferentes unidades
* Acompanhar o histórico completo de cada item

## Conceitos Fundamentais

### Estrutura Hierárquica

O sistema GNRX organiza o estoque em uma estrutura hierárquica:

```
Item (Tipo de EPI)
 └── Lotes (Grupos de itens adquiridos juntos)
      └── Itens Individuais (Unidades físicas específicas)
           └── Variantes (Tamanhos, cores, etc. quando aplicável)
```

### Numeração e Identificação

Cada lote recebe uma identificação única:

* **Número do Lote**: Geralmente no formato CA\[Número do CA]-L\[Sequencial]
* **Exemplo**: CA43350-L02

Cada item individual dentro do lote recebe:

* **Número de Série**: Identificador único no formato \[Número do Lote]-\[Sequencial]
* **Exemplo**: CA43350-L02-00000001

## Informações Gerenciadas

Para cada lote, o sistema controla:

* **Dados básicos**: Número do lote, quantidade total, custo unitário
* **Informações financeiras**: Valor total do lote, valor em estoque
* **Controle de validade**: Data de validade, dias até vencimento
* **Distribuição**: Alocação por unidade e por variante (quando aplicável)
* **Status**: Quantidades disponíveis, em uso, total

## Interface Principal

A tela de lotes apresenta:

* **Resumo do lote**: Quantidade total, disponível e em uso
* **Informações financeiras**: Custo unitário, valor total
* **Detalhes de validade**: Data de vencimento, dias restantes
* **Lista de itens**: Detalhamento de cada unidade física
* **Distribuição**: Alocação por unidade/local

## Tipos de Fluxo

O sistema oferece dois fluxos principais para adição de lotes, dependendo da configuração do item:

### 1. Fluxo para Itens sem Variantes

Processo simplificado com foco apenas na quantidade total e distribuição por unidade.

### 2. Fluxo para Itens com Variantes

Processo mais detalhado que inclui a distribuição por variantes (tamanho, cor, etc.) e posteriormente por unidade.

## Ciclo de Vida do Lote

Um lote típico passa pelas seguintes etapas:

1. **Criação**: Registro inicial no sistema
2. **Distribuição**: Alocação entre unidades
3. **Utilização**: Atribuição de itens a colaboradores
4. **Devoluções**: Retorno de itens ao estoque
5. **Gestão de validade**: Monitoramento de prazos
6. **Baixa**: Quando todos os itens são consumidos ou expiram

## Próximos Passos

Para gerenciar efetivamente os lotes no Sistema GNRX, consulte os seguintes guias:

* [Adicionar Lote](adicionar-lote.md) - Como registrar novos lotes no sistema
* [Adicionar Lote sem Variantes](adicionar-lote-sem-variantes.md) - Processo simplificado para itens sem variantes
* [Adicionar Lote com Variantes](adicionar-lote-com-variantes.md) - Processo detalhado para itens com variantes
* [Editar Lote](editar-lote.md) - Como atualizar informações de lotes existentes
* [Visualizar Itens do Lote](visualizar-items-lote.md) - Como verificar unidades individuais
* [Gerenciar Validade](gerenciar-validade.md) - Como controlar datas de vencimento

***

_Última atualização: 18 de Maio de 2025_
