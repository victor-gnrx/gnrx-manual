# Vincular Unidades

Esta página explica como associar setores a unidades no Sistema GNRX Gestão de EPI.

## Visão Geral

A vinculação entre setores e unidades é uma configuração fundamental no sistema, permitindo que um mesmo setor (área funcional) exista em diferentes localidades físicas da empresa. Esta associação determina onde os colaboradores podem ser alocados e como os EPIs serão distribuídos.

## Conceito de Vínculo Setor-Unidade

No Sistema GNRX:
- Uma **Unidade** representa uma localidade física (filial, planta, escritório)
- Um **Setor** representa uma área funcional (departamento, equipe)
- Um mesmo setor pode existir em múltiplas unidades
- Cada colaborador é vinculado a um setor dentro de uma unidade específica

![Conceito de Vínculo](../../../assets/images/conceito-vinculo-setor-unidade.png)

## Acessando a Tela de Vinculação

Existem duas formas de gerenciar os vínculos entre setores e unidades:

### Opção 1: A partir do Setor

1. No menu lateral, clique em **Estruturas**
2. Selecione **Setores**
3. Clique no setor desejado para abrir a tela de detalhes
4. Selecione a aba **Unidades**

![Acesso via Setor](../../../assets/images/setor-aba-unidades.png)

### Opção 2: A partir da Unidade

1. No menu lateral, clique em **Estruturas**
2. Selecione **Unidades**
3. Clique na unidade desejada para abrir a tela de detalhes
4. Selecione a aba **Setores**
5. Clique em **Adicionar Setor**

![Acesso via Unidade](../../../assets/images/unidade-aba-setores.png)

## Visualizando Unidades Vinculadas a um Setor

Na tela de detalhes do setor, a aba **Unidades** exibe:

![Unidades do Setor](../../../assets/images/unidades-do-setor.png)

- Lista das unidades onde o setor está presente
- Quantidade de colaboradores do setor em cada unidade
- Data de vinculação (quando disponível)

Esta visualização permite uma rápida avaliação da distribuição do setor pela empresa.

## Vinculando um Setor a uma Unidade

### A partir do Setor

1. Na tela de detalhes do setor, selecione a aba **Unidades**
2. Clique no botão **Vincular a Unidades**
3. No modal exibido, selecione as unidades desejadas na lista
4. Clique em **Confirmar** para estabelecer as vinculações

![Vincular a partir do Setor](../../../assets/images/vincular-unidades-setor.png)

### A partir da Unidade

1. Na tela de detalhes da unidade, selecione a aba **Setores**
2. Clique no botão **Adicionar Setor**
3. No modal exibido, selecione os setores desejados na lista
4. Clique em **Confirmar** para estabelecer as vinculações

![Vincular a partir da Unidade](../../../assets/images/vincular-setores-unidade.png)

## Removendo Vínculo entre Setor e Unidade

### A partir do Setor

1. Na tela de detalhes do setor, selecione a aba **Unidades**
2. Localize a unidade que deseja desvincular
3. Clique no ícone de remoção (lixeira)
4. Confirme a ação no diálogo exibido

### A partir da Unidade

1. Na tela de detalhes da unidade, selecione a aba **Setores**
2. Localize o setor que deseja desvincular
3. Clique no ícone de remoção (lixeira)
4. Confirme a ação no diálogo exibido

> **Importante:** A remoção de vínculo só é possível quando não há colaboradores associados ao setor na unidade específica.

## Impacto da Vinculação

A vinculação entre setores e unidades tem os seguintes impactos no sistema:

- Define onde os colaboradores podem ser alocados
- Determina a disponibilidade de setores para seleção em formulários
- Afeta a organização de relatórios e estatísticas
- Influencia a distribuição e gestão de EPIs

## Verificações e Alertas

Ao vincular ou desvincular setores e unidades, o sistema realiza as seguintes verificações:

| Verificação | Alerta | Impacto |
|-------------|--------|---------|
| Colaboradores existentes | "Existem colaboradores vinculados a este setor na unidade" | Impede a remoção do vínculo |
| GHEs específicos | "Existem GHEs vinculados a este setor na unidade" | Aviso antes da remoção |
| Solicitações pendentes | "Existem solicitações pendentes para este setor na unidade" | Aviso antes da remoção |

## Melhores Práticas

Para uma gestão eficiente dos vínculos entre setores e unidades:

- Configure todos os vínculos necessários antes de cadastrar colaboradores
- Mantenha a mesma estrutura de setores entre unidades similares para facilitar comparações
- Revise periodicamente os vínculos para garantir que refletem a estrutura atual da empresa
- Documente a razão de vinculações específicas quando não forem óbvias
- Considere o impacto na gestão de EPIs ao criar ou remover vínculos

## Vinculação em Massa

Para empresas com muitas unidades e setores, é possível realizar vinculação em massa:

1. No menu **Estruturas**, selecione **Gerenciamento de Estrutura**
2. Acesse a aba **Vínculos em Massa**
3. Utilize a matriz para selecionar múltiplos vínculos de uma só vez
4. Clique em **Aplicar Alterações** para confirmar

## Relatórios e Análises

O sistema oferece relatórios específicos sobre a distribuição de setores por unidades:

1. No menu **Relatórios**, selecione **Estrutura Organizacional**
2. Escolha o relatório **Distribuição de Setores**
3. Aplique filtros conforme necessário
4. Gere o relatório para visualizar a distribuição completa

Este relatório é útil para análise organizacional e planejamento de EPIs.

---

*Última atualização: 16 de Maio de 2025*