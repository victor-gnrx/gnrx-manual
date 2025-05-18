# Adicionar Lote

Esta página explica o processo de adição de um novo lote de EPIs ao estoque no Sistema GNRX.

## Visão Geral

O registro de lotes é essencial para o controle eficiente do estoque de EPIs, permitindo rastreabilidade, gestão de validade e acompanhamento detalhado de cada grupo de produtos recebidos. Cada lote representa uma entrada específica de EPIs no estoque, com suas características particulares como data de recebimento, quantidade, fabricante e validade.

## Acessando a Tela de Adição de Lote

Existem duas formas de acessar a tela de adição de lote:

### Opção 1: A partir da Gestão de Estoque

1. No menu lateral, acesse **Gestão de Estoque**
2. Selecione **Lotes**
3. Clique no botão **Adicionar Lote**

### Opção 2: A partir de um Item Específico

1. No menu lateral, acesse **Gestão de Estoque**
2. Selecione **Itens**
3. Localize o item desejado e clique em **Detalhes**
4. Na aba **Lotes**, clique em **Adicionar Lote**

![Adicionar Lote Botão](../../../assets/images/adicionar-lote-botao.png)

## Processo de Adição de Lote

### Passo 1: Seleção do Item (se acessado via Gestão de Estoque)

![Seleção de Item](../../../assets/images/lote-selecao-item.png)

1. Utilize a barra de pesquisa para localizar o item
2. Selecione o item desejado na lista de resultados

### Passo 2: Preenchimento das Informações do Lote

![Formulário de Lote](../../../assets/images/lote-formulario.png)

| Campo | Descrição | Obrigatório |
|-------|-----------|-------------|
| Número do Lote | Identificador único do lote (geralmente fornecido pelo fabricante) | Sim |
| Data de Recebimento | Data em que o lote foi recebido pela empresa | Sim |
| Quantidade Total | Número total de unidades recebidas neste lote | Sim |
| Custo Unitário | Valor unitário de cada item em R$ (centavos) | Sim |
| Data de Validade | Data limite para utilização dos EPIs deste lote | Depende* |

> *Obrigatório apenas para itens com controle de validade ativado.

### Passo 3: Configuração de Variantes (se aplicável)

![Configuração de Variantes do Lote](../../../assets/images/lote-variantes.png)

Se o item possuir variantes configuradas (como tamanho, cor, etc.):

1. O sistema exibirá uma tabela para distribuição da quantidade total entre as variantes
2. Preencha a quantidade para cada combinação de variantes
3. Certifique-se de que o total das quantidades distribuídas seja igual à quantidade total informada anteriormente

### Passo 4: Detalhamento de Unidades (opcional)

![Detalhamento de Unidades](../../../assets/images/lote-detalhamento.png)

Para EPIs com controle individualizado (como capacetes, cintos de segurança):

1. Marque a opção **Detalhar Unidades Individuais**
2. Para cada unidade, você poderá informar:
   - Número de série (se aplicável)
   - Características específicas
   - Observações individuais

### Passo 5: Finalização

1. Revise todas as informações preenchidas
2. Clique no botão **Salvar Lote**
3. O sistema exibirá uma mensagem de confirmação
4. O novo lote será adicionado ao estoque, aumentando a quantidade disponível do item

## Impacto no Estoque

Ao adicionar um novo lote, o sistema automaticamente:

1. Incrementa o estoque disponível do item
2. Registra a entrada no histórico de movimentações
3. Adiciona o lote à lista de lotes ativos para o item
4. Atualiza os alertas de estoque mínimo, se aplicável
5. Configura alertas de validade, se aplicável

## Considerações Importantes

### Gestão de Validade

Para itens com controle de validade ativado:

- O sistema alertará quando a data de validade estiver próxima
- EPIs com validade inferior a 30 dias serão destacados nos relatórios
- A data de validade impactará a ordem de utilização dos itens (FEFO - First Expired, First Out)

### Controle de Custos

O valor informado no lote é utilizado para:

- Cálculo do custo médio do item
- Valoração do estoque
- Análise financeira de consumo por setor/colaborador
- Projeções de orçamento para aquisições futuras

### Rastreabilidade

O lote permite rastrear:

- Origem dos EPIs em caso de problemas
- Quais colaboradores receberam itens de determinado lote
- Histórico completo do ciclo de vida dos equipamentos

## Erros Comuns e Soluções

| Erro | Solução |
|------|---------|
| "Número de lote já existente" | Verifique se o lote já foi cadastrado ou use um identificador diferente |
| "Total de variantes não corresponde à quantidade total" | Ajuste as quantidades para que a soma das variantes seja igual à quantidade total |
| "Data de validade inválida" | Verifique se a data está no formato correto e é posterior à data atual |
| "Custo unitário inválido" | Verifique se o valor está em centavos e não contém caracteres especiais |

## Melhores Práticas

- Padronize a nomenclatura dos lotes para facilitar a identificação
- Registre lotes separados para EPIs com datas de validade diferentes
- Sempre verifique a integridade dos itens antes de registrar a entrada no sistema
- Utilize a área de observações para registrar informações relevantes sobre a aquisição
- Mantenha os custos atualizados para refletir o valor real de reposição