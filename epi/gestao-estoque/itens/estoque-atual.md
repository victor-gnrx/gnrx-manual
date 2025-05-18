# Estoque Atual

Esta página explica como acessar e utilizar o relatório de Estoque Atual no Sistema GNRX.

## Visão Geral

O relatório de Estoque Atual oferece uma visão completa e atualizada de todos os EPIs disponíveis, permitindo monitorar quantidades, identificar itens com estoque baixo e gerenciar eficientemente o inventário de equipamentos de proteção.

## Acessando o Relatório

1. No menu lateral, acesse **Gestão de Estoque**
2. Selecione **Relatórios**
3. Clique em **Estoque Atual**

![Acesso ao Relatório de Estoque](../../../assets/images/acesso-relatorio-estoque.png)

## Interface do Relatório

![Interface do Relatório de Estoque](../../../assets/images/interface-relatorio-estoque.png)

O relatório de Estoque Atual apresenta:

### Filtros e Controles

| Filtro | Descrição |
|--------|-----------|
| Unidade | Filtra o estoque por unidade específica |
| Tipo de EPI | Filtra por categoria de EPI conforme NR-6 |
| Status de Estoque | Todos, Crítico (abaixo do mínimo), Normal |
| Mostrar Variantes | Expandir para mostrar detalhamento por variante |
| Incluir Inativos | Mostra também itens marcados como inativos |

### Tabela de Resultados

A tabela principal exibe:

- **Código**: Identificador único do item
- **Nome**: Nome descritivo do EPI
- **CA**: Número do Certificado de Aprovação (quando aplicável)
- **Estoque Mínimo**: Nível mínimo configurado
- **Estoque Atual**: Quantidade disponível atualmente
- **Status**: Indicativo visual (Verde: normal, Amarelo: baixo, Vermelho: crítico)
- **Valor Médio**: Custo unitário médio (baseado nos lotes)
- **Valor Total**: Valor total do estoque deste item

### Resumo Estatístico

No topo do relatório, são apresentados indicadores resumidos:

- Total de itens em estoque
- Valor total do inventário
- Quantidade de itens em nível crítico
- Valor total de itens a repor (baseado no estoque mínimo)

## Funcionalidades Avançadas

### Visualização Detalhada

Ao clicar em um item da lista, o sistema exibe informações detalhadas:

- Distribuição por lote (quantidades e validades)
- Detalhamento por variante (tamanhos, cores, etc.)
- Histórico recente de movimentações
- Gráfico de evolução do estoque nos últimos meses

![Detalhamento de Item](../../../assets/images/detalhamento-item-estoque.png)

### Exportação de Dados

O relatório pode ser exportado em diversos formatos:

1. Clique no botão **Exportar**
2. Selecione o formato desejado:
   - Excel (.xlsx)
   - CSV
   - PDF
3. Escolha as colunas a incluir
4. Defina o nome do arquivo
5. Clique em **Confirmar Exportação**

### Impressão Formatada

Para imprimir o relatório:

1. Clique no botão **Imprimir**
2. Escolha entre:
   - Resumido: apenas os totais principais
   - Completo: todos os itens com detalhes
   - Críticos: apenas itens abaixo do estoque mínimo
3. Ajuste as opções de impressão conforme necessário
4. Clique em **Confirmar Impressão**

## Alertas e Notificações

O sistema GNRX pode gerar alertas automáticos baseados neste relatório:

- **Alertas de Estoque Mínimo**: Notificação quando um item atinge o nível mínimo configurado
- **Previsão de Esgotamento**: Aviso antecipado baseado na taxa de consumo histórica
- **Lembrete de Reposição**: Sugestão de pedido de compra para itens críticos

Para configurar estes alertas:
1. No menu lateral, acesse **Configurações Gerais**
2. Selecione **Alertas e Notificações**
3. Configure os parâmetros desejados na seção **Estoque**

## Análise de Dados

Além da visualização direta, o relatório oferece ferramentas de análise:

### Gráficos de Distribuição

![Gráficos de Distribuição](../../../assets/images/graficos-distribuicao-estoque.png)

- Distribuição de estoque por categoria de EPI
- Representação de valor por tipo de equipamento
- Comparativo entre estoque atual e estoque mínimo

### Análise de Tendências

![Análise de Tendências](../../../assets/images/tendencias-estoque.png)

- Evolução do estoque nos últimos períodos
- Projeção de consumo baseada em histórico
- Identificação de sazonalidades

### Análise ABC

O relatório permite classificar os itens conforme a análise ABC:
- **Classe A**: Itens de alto valor que representam cerca de 20% do inventário e 80% do valor
- **Classe B**: Itens de valor intermediário
- **Classe C**: Itens de baixo valor que representam a maioria do inventário mas pequena parcela do valor

Esta classificação ajuda a priorizar a gestão de estoque nos itens mais significativos.

## Planejamento de Compras

Com base nos dados do relatório, o sistema oferece suporte ao planejamento de compras:

![Planejamento de Compras](../../../assets/images/planejamento-compras.png)

1. Clique no botão **Gerar Sugestão de Compra**
2. O sistema analisará:
   - Itens abaixo do estoque mínimo
   - Taxa de consumo histórica
   - Tempo médio de entrega dos fornecedores
3. Será gerada uma lista de itens a adquirir com:
   - Quantidade sugerida
   - Valor estimado
   - Prioridade de compra
   - Fornecedores potenciais

Esta funcionalidade otimiza o processo de reposição, evitando tanto a falta quanto o excesso de itens em estoque.

## Melhores Práticas

### Monitoramento Regular

- Consulte o relatório de Estoque Atual semanalmente
- Configure alertas automáticos para níveis críticos
- Revise periodicamente os níveis de estoque mínimo com base no consumo real

### Inventário Físico

- Realize contagens físicas periódicas para validar as informações do sistema
- Utilize a funcionalidade "Ajuste de Estoque" para corrigir eventuais discrepâncias
- Documente os motivos dos ajustes para análises futuras

### Análise Integrada

- Compare os dados de estoque com informações de:
  - Solicitações pendentes
  - Entregas programadas
  - Previsão de admissões/demissões
  - Mudanças sazonais nas atividades

Estas análises permitem uma gestão proativa e mais eficiente do estoque de EPIs.