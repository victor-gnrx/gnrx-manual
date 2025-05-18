# Configurar Tipos de Variante

Esta página explica como configurar tipos de variantes para itens de EPI no Sistema GNRX, permitindo o controle preciso de diferentes versões do mesmo equipamento (como tamanhos, cores, modelos).

## O que são Variantes?

Variantes são características que diferenciam versões do mesmo EPI. Por exemplo, um capacete de proteção pode ter variantes de cor (branco, amarelo, vermelho) e tamanho (P, M, G). Configurar corretamente as variantes permite:

- Controle específico de estoque para cada versão
- Entrega do EPI exatamente adequado para cada colaborador
- Rastreabilidade detalhada de cada unidade

## Acessando a Configuração de Variantes

Há duas formas de acessar a configuração de variantes:

### 1. Durante o cadastro de um novo item

Ao finalizar o cadastro de um novo item com a opção "Este item possui variantes" marcada, o sistema direcionará automaticamente para a tela de configuração de variantes.

### 2. Para um item já existente

1. No menu lateral, acesse **Gestão de Estoque**
2. Selecione **Itens**
3. Localize o item desejado e clique no ícone de **Editar**
4. Na tela de edição, clique na aba **Variantes**

![Acesso às Variantes](../../../assets/images/acesso-variantes.png)

## Configurando Tipos de Variante

### Passo 1: Adicionar um Tipo de Variante

1. Na seção "Tipos de Variante", clique no botão **Adicionar Tipo**
2. Preencha o formulário com as seguintes informações:

![Cadastro de Tipo de Variante](../../../assets/images/tipo-variante-form.png)

| Campo | Descrição | Exemplo |
|-------|-----------|---------|
| Nome | Nome descritivo do tipo de variante | "Tamanho" |
| Obrigatório | Se é obrigatório especificar esta variante | Sim/Não |
| Ordem | Número que define a ordem de exibição/seleção | 1, 2, 3... |

3. Clique em **Salvar Tipo**

### Passo 2: Adicionar Valores para o Tipo de Variante

Após criar um tipo de variante, é necessário definir os valores possíveis para esse tipo:

1. Na linha do tipo de variante criado, clique no botão **Valores**
2. Na tela de valores, clique em **Adicionar Valor**
3. Preencha o formulário:

![Cadastro de Valor de Variante](../../../assets/images/valor-variante-form.png)

| Campo | Descrição | Exemplo |
|-------|-----------|---------|
| Valor | O valor específico da variante | "P", "M", "G" ou "Vermelho", "Azul" |
| Ordem | Número que define a ordem de exibição/seleção | 1, 2, 3... |

4. Clique em **Salvar Valor**
5. Repita o processo para adicionar todos os valores possíveis para este tipo de variante

### Passo 3: Repita o Processo para Outros Tipos de Variante (Se Necessário)

Se o item possuir múltiplos tipos de variantes (ex: tamanho E cor), repita os passos 1 e 2 para cada tipo adicional.

## Exemplo Prático: Configurando Variantes para uma Luva de Proteção

### Cenário

Uma luva de proteção com variantes de tamanho (P, M, G, GG) e cor (Amarela, Preta).

### Configuração

1. **Primeiro Tipo de Variante**:
   - Nome: Tamanho
   - Obrigatório: Sim
   - Ordem: 1
   - Valores: P (1), M (2), G (3), GG (4)

2. **Segundo Tipo de Variante**:
   - Nome: Cor
   - Obrigatório: Sim
   - Ordem: 2
   - Valores: Amarela (1), Preta (2)

## Impacto no Estoque

Ao configurar variantes, o sistema criará combinações únicas para controle de estoque. No exemplo da luva, seriam criadas as seguintes combinações:

- Luva Tamanho P / Cor Amarela
- Luva Tamanho P / Cor Preta
- Luva Tamanho M / Cor Amarela
- Luva Tamanho M / Cor Preta
- Luva Tamanho G / Cor Amarela
- Luva Tamanho G / Cor Preta
- Luva Tamanho GG / Cor Amarela
- Luva Tamanho GG / Cor Preta

Cada combinação terá seu próprio controle de estoque e poderá ser rastreada individualmente.

## Observações Importantes

- A configuração de variantes deve ser feita antes de registrar entradas de estoque
- Não é possível remover tipos de variantes após o item já possuir movimentações de estoque
- Utilize a ordem para definir a sequência lógica de seleção (geralmente tamanho vem antes de cor)
- Limite-se às variantes realmente necessárias para não complicar desnecessariamente a gestão
- As variantes definidas aqui serão utilizadas durante a solicitação de EPIs para seleção do item específico para cada colaborador