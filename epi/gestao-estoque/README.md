# Gestão de Estoque

O módulo de Gestão de Estoque do Sistema GNRX permite o controle completo e eficiente de todos os Equipamentos de Proteção Individual disponíveis na organização, desde o cadastro inicial até a movimentação e acompanhamento de níveis de estoque.

## Visão Geral

Uma gestão eficiente do estoque de EPIs é fundamental para garantir:
- Disponibilidade constante dos equipamentos necessários
- Controle de validade e vida útil dos EPIs
- Rastreabilidade completa das movimentações
- Otimização de recursos financeiros
- Conformidade com requisitos legais

![Painel de Gestão de Estoque](../assets/images/painel-gestao-estoque.png)

## Componentes Principais

### Itens de EPI

O cadastro de itens é a base da gestão de estoque, permitindo registrar todos os tipos de EPIs utilizados pela organização, com ou sem Certificado de Aprovação (CA).

[Saiba mais sobre o gerenciamento de Itens](./itens/README.md)

### Variantes

O sistema permite configurar variantes para cada item (como tamanhos, cores, modelos), facilitando o controle preciso do estoque e a entrega do equipamento correto para cada colaborador.

[Saiba mais sobre o gerenciamento de Variantes](./variantes/README.md)

### Lotes

O controle por lotes permite o acompanhamento de grupos específicos de EPIs, facilitando a gestão de validade, rastreabilidade em caso de defeitos e controle de qualidade.

[Saiba mais sobre o gerenciamento de Lotes](./lotes/README.md)

### Relatórios

O módulo oferece diversos relatórios para análise e tomada de decisão, como níveis atuais de estoque, previsão de consumo, itens próximos do vencimento e histórico de movimentações.

[Saiba mais sobre os Relatórios disponíveis](./relatorios/README.md)

## Funcionalidades Principais

### Controle de Níveis de Estoque

- Monitoramento em tempo real das quantidades disponíveis
- Alertas automáticos para níveis mínimos de estoque
- Estatísticas de consumo para planejamento de compras

### Gestão de Validade

- Acompanhamento das datas de validade de cada item
- Alertas para itens próximos do vencimento
- Priorização automática de itens com prazo de validade menor (FIFO/FEFO)

### Rastreabilidade

- Identificação de lotes e números de série
- Histórico completo de movimentações
- Vinculação entre itens em estoque e colaboradores que os receberam

### Controle de Custos

- Registro de valores de aquisição
- Análise de custo por colaborador, setor e unidade
- Relatórios financeiros para planejamento orçamentário

## Fluxo de Trabalho Recomendado

Para uma gestão eficiente do estoque de EPIs, recomendamos seguir este fluxo de trabalho:

1. Cadastrar os itens de EPI com todas as suas características
2. Configurar variantes quando aplicável (tamanhos, cores, etc.)
3. Registrar a entrada de novos lotes no estoque
4. Monitorar regularmente os níveis de estoque e datas de validade
5. Utilizar os relatórios para planejar novas aquisições
6. Manter o inventário atualizado com contagens periódicas

## Boas Práticas

- Realize inventários físicos periodicamente para validar as informações do sistema
- Configure corretamente os níveis mínimos de estoque para cada item
- Utilize códigos de barras ou QR codes para facilitar a identificação e movimentação de itens
- Estabeleça processos claros para solicitação, aprovação e registro de saídas de estoque
- Monitore os relatórios de consumo para identificar padrões e otimizar o estoque