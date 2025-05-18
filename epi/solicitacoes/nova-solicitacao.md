# Nova Solicitação

Esta página detalha o processo para criar uma nova solicitação de EPI para um colaborador no Sistema GNRX.

## Visão Geral

A criação de uma solicitação é o primeiro passo do fluxo de entrega de EPIs. Uma solicitação bem detalhada garante que o colaborador receba o equipamento correto e que todo o processo seja devidamente documentado para fins de conformidade legal.

## Acessando a Tela de Nova Solicitação

1. No menu lateral, acesse **Solicitações**
2. Clique no botão **Nova Solicitação** no canto superior direito

![Nova Solicitação Botão](../../../assets/images/nova-solicitacao-botao.png)

## Processo de Criação

O processo de criação de uma nova solicitação é dividido em 4 etapas:

### Etapa 1: Seleção do Colaborador

![Seleção de Colaborador](../../../assets/images/solicitacao-selecao-colaborador.png)

1. Utilize a barra de pesquisa para localizar o colaborador por nome, CPF ou matrícula
2. Alternativamente, selecione um colaborador da lista exibida
3. Para filtrar a lista, você pode selecionar uma unidade e/ou setor específico
4. Clique no nome do colaborador desejado para selecioná-lo
5. Após a seleção, o sistema exibirá informações básicas do colaborador e seu histórico recente de EPIs
6. Clique em **Próximo** para avançar

> **Nota:** Se o colaborador possuir itens pendentes de devolução, o sistema exibirá um alerta. Você pode prosseguir mesmo assim, mas é recomendável regularizar as devoluções pendentes primeiro.

### Etapa 2: Seleção dos EPIs

![Seleção de EPIs](../../../assets/images/solicitacao-selecao-epis.png)

1. O sistema apresentará automaticamente os EPIs recomendados com base no GHE do colaborador
2. Você pode adicionar EPIs recomendados clicando no botão **+** ao lado de cada item
3. Para adicionar EPIs não listados nas recomendações:
   - Clique no botão **Adicionar Outro EPI**
   - Utilize a barra de pesquisa para localizar o item desejado
   - Selecione o item na lista de resultados
4. Para cada EPI adicionado:
   - Defina a quantidade (geralmente 1, a menos que sejam itens de consumo como luvas descartáveis)
   - Selecione as variantes, se existirem (tamanho, cor, etc.)
5. Você pode remover um item adicionado clicando no ícone de lixeira
6. Após selecionar todos os EPIs necessários, clique em **Próximo**

### Etapa 3: Definição de Motivos

![Definição de Motivos](../../../assets/images/solicitacao-motivos.png)

Para cada EPI selecionado, é necessário definir o motivo da solicitação:

1. Selecione um motivo na lista suspensa para cada item
   - Primeira Entrega (Nunca recebeu este item)
   - Substituição por Desgaste
   - Substituição por Perda
   - Substituição por Quebra
   - Substituição por Validade Vencida
   - Outros
2. Se selecionar "Outros", um campo adicional para detalhamento aparecerá
3. Após definir todos os motivos, clique em **Próximo**

> **Dica:** Os motivos disponíveis podem ser personalizados nas [Configurações de Motivos](../../configuracoes-gerais/motivos/motivos-solicitacao.md).

### Etapa 4: Observações e Finalização

![Finalização](../../../assets/images/solicitacao-finalizacao.png)

1. Adicione observações gerais sobre a solicitação, se necessário
2. Revise todos os itens, quantidades e motivos
3. Clique no botão **Finalizar Solicitação**
4. O sistema exibirá uma mensagem de confirmação com o número da solicitação
5. Você pode então:
   - Visualizar a solicitação criada
   - Imprimir um comprovante de solicitação
   - Criar uma nova solicitação
   - Voltar à lista de solicitações

## Confirmação da Solicitação

Após finalizada, a solicitação ficará com o status "Pendente" e estará disponível para processamento na tela de [Pendentes de Entrega](../entrega/pendentes-entrega.md).

## Solicitações Urgentes

Para casos que exigem entrega imediata:

1. Na tela de finalização, marque a opção **Solicitação Urgente**
2. Adicione a justificativa da urgência no campo correspondente
3. Solicitações marcadas como urgentes recebem destaque especial na lista de pendentes

## Possíveis Erros e Soluções

| Erro | Solução |
|------|---------|
| "Colaborador não encontrado" | Verifique se o colaborador está ativo no sistema |
| "Item sem estoque disponível" | Verificar disponibilidade no estoque ou providenciar aquisição |
| "Item incompatível com o GHE" | Verificar se o EPI selecionado é adequado para os riscos do colaborador |
| "Variante não especificada" | Selecionar todas as variantes obrigatórias (tamanho, cor, etc.) |

## Melhores Práticas

- Prefira sempre seguir as recomendações automáticas baseadas no GHE
- Mantenha os motivos de solicitação precisos para análises estatísticas corretas
- Faça uma solicitação separada caso um mesmo colaborador precise de EPIs para funções diferentes
- Inclua observações relevantes que possam facilitar a entrega e orientação ao colaborador