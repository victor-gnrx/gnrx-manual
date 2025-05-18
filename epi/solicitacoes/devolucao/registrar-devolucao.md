# Registrar Devolução

Esta página explica como processar a devolução de EPIs previamente entregues a colaboradores no Sistema GNRX.

## Visão Geral

O processo de devolução é uma etapa fundamental na gestão do ciclo de vida dos EPIs, permitindo recuperar equipamentos que ainda possuem vida útil, controlar adequadamente os itens que precisam ser descartados e manter o histórico completo de movimentações.

## Tipos de Devolução

O Sistema GNRX reconhece três principais tipos de devolução:

1. **Devolução Normal**: O EPI é devolvido em condições adequadas de uso
2. **Registro de Perda**: O colaborador relata que o EPI foi perdido ou extraviado
3. **Registro de Quebra**: O EPI é devolvido, mas está danificado ou inadequado para reuso

## Acessando a Tela de Devolução

### Opção 1: A partir da Lista de Itens Pendentes

1. No menu lateral, acesse **Solicitações**
2. Selecione **Devoluções**
3. Na aba **Itens Pendentes**, localize o colaborador ou item desejado
4. Clique no botão **Registrar Devolução**

### Opção 2: A partir do Perfil do Colaborador

1. Acesse o perfil do colaborador
2. Clique na aba **EPIs Pendentes**
3. Localize o item desejado e clique em **Registrar Devolução**

![Acesso à Devolução](../../../assets/images/acesso-devolucao.png)

## Processo de Devolução

### Passo 1: Seleção dos Itens para Devolução

![Seleção de Itens para Devolução](../../../assets/images/selecao-itens-devolucao.png)

1. O sistema apresentará todos os EPIs pendentes de devolução do colaborador
2. Marque os itens que estão sendo devolvidos naquele momento
3. Para cada item, selecione o tipo de devolução (Normal, Perda ou Quebra)
4. Clique em **Prosseguir**

### Passo 2: Detalhamento por Tipo de Devolução

Dependendo do tipo selecionado, o sistema solicitará informações específicas:

#### Para Devolução Normal

![Devolução Normal](../../../assets/images/devolucao-normal.png)

1. Estado de conservação (Ótimo, Bom, Regular, Ruim)
2. Observações (opcional)
3. Indicação se o item pode retornar ao estoque

#### Para Registro de Perda

![Registro de Perda](../../../assets/images/registro-perda.png)

1. Motivo da perda (selecione na lista predefinida)
2. Descrição detalhada das circunstâncias
3. Data aproximada da perda
4. Indicação se haverá cobrança/ressarcimento

#### Para Registro de Quebra

![Registro de Quebra](../../../assets/images/registro-quebra.png)

1. Motivo da quebra (selecione na lista predefinida)
2. Descrição do dano
3. Indicação se o dano foi causado por uso inadequado
4. Possibilidade de anexar foto do item danificado

### Passo 3: Confirmação da Devolução

![Confirmação de Devolução](../../../assets/images/confirmacao-devolucao.png)

1. Revise todas as informações preenchidas
2. Adicione observações gerais, se necessário
3. Clique em **Confirmar Devolução**
4. O sistema exibirá uma mensagem de confirmação e atualizará o status dos itens

## Impacto no Estoque

O tratamento dos itens devolvidos varia conforme o tipo de devolução:

| Tipo de Devolução | Impacto no Estoque | Tratamento |
|-------------------|---------------------|------------|
| Devolução Normal (Bom estado) | Retorna ao estoque disponível | Item pode ser reutilizado para novas entregas |
| Devolução Normal (Estado ruim) | Não retorna ao estoque | Item registrado como "Descartado" |
| Registro de Perda | Baixa definitiva | Item registrado como "Perdido" |
| Registro de Quebra | Baixa definitiva | Item registrado como "Danificado" |

## Registros e Documentação

Cada devolução gera:

1. Atualização na Ficha de EPI Digital do colaborador
2. Registro no histórico de movimentação do item
3. Atualização nos relatórios de conformidade
4. Documentação da devolução com data, hora e responsável pelo recebimento

## Observações Importantes

### Prazos de Devolução

- O sistema destaca automaticamente itens com prazo de devolução vencido
- Para itens de uso permanente, a devolução só é exigida em caso de substituição ou desligamento
- Para itens com uso temporário, o sistema calcula a data esperada de devolução com base na configuração do item

### Perda Recorrente

O sistema monitora padrões de perda e pode gerar alertas quando um colaborador registra perdas frequentes, permitindo ações preventivas ou educativas.

### Quebras Sistemáticas

Um número elevado de quebras para determinado modelo de EPI pode indicar problemas de qualidade, proporcionando dados para reavaliação de fornecedores.

## Melhores Práticas

- Realize a devolução o mais breve possível após o recebimento físico do item
- Documente detalhadamente as condições de itens danificados
- Utilize fotos para registrar danos quando relevante
- Estabeleça critérios claros para determinar quando um item pode retornar ao estoque
- Não aceite devoluções de EPIs descartáveis ou de uso único
- Verifique se o item devolvido corresponde exatamente ao que foi entregue (mesmo modelo, tamanho, etc.)