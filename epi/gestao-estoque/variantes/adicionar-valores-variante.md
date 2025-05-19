# Adicionar Valores de Variante

Esta página explica como adicionar valores a variantes de itens de EPI no Sistema GNRX Gestão de EPI.

## Visão Geral

Após criar um tipo de variante, é necessário definir os valores específicos que essa variante pode assumir, como tamanhos, cores ou materiais. Esta etapa é essencial para adequar cada item às diversas necessidades dos colaboradores.

![Adicionar Valores de Variante](../../../assets/images/adicionar-valores-variante.png)

## Acesso à Adição de Valores

Para adicionar valores a uma variante:

1. Acesse o módulo **Inventário**
2. Clique no item desejado na lista para abrir seus detalhes
3. Navegue até a aba **Informações Item**
4. Na seção "Variantes do Item", clique no botão **Adicionar Variante** para criar uma nova, ou selecione uma variante existente para adicionar mais valores

## Utilização de Categorias Pré-configuradas

O sistema oferece valores pré-definidos para facilitar o cadastro:

### Selecionando a Categoria

1. Escolha a categoria apropriada nas abas superiores:
   - **Vestuário**: Para roupas e uniformes
   - **Calçados**: Para sapatos e botas
   - **Cores**: Para definir opções de cores
   - **Materiais**: Para especificar materiais de fabricação
   - **Medidas**: Para dimensões específicas

2. Selecione a subcategoria quando disponível:
   - **Tamanho (Vestuário)** ou **Tamanho (Infantil)**
   - **Cor (Básicas)** ou **Cor (Vibrantes)**

## Adicionando Valores Específicos

Para cada tipo de variante, você pode:

1. Digitar o **Nome da Variante** (ex: "Tamanho", "Cor", "Material")
2. Definir se é **Obrigatória** ativando ou não o toggle
3. Adicionar os **Valores da Variante**:
   - Digite cada valor no campo disponível
   - Clique no botão **+ Adicionar** para incluir mais campos
   - Use o botão **Excluir todos** para remover todos os valores

### Valores Comuns por Categoria

Cada categoria apresenta valores pré-configurados que podem ser usados como referência:

#### Vestuário
- **Tamanho (Vestuário)**: PP, P, M, G, GG, XG
- **Tamanho (Infantil)**: 2, 4, 6, 8, 10, 12, 14, 16

#### Calçados
- **Tamanho (Calçado)**: 32, 33, 34, 35, 36, 37, 38, 39, 40, 41, 42, 43, 44

#### Cores
- **Cor (Básicas)**: Preto, Branco, Cinza, Bege, Marrom
- **Cor (Vibrantes)**: Vermelho, Azul, Verde, Amarelo, Roxo, Rosa, Laranja

#### Materiais
- **Material**: Algodão, Poliéster, Nylon, Linho, Jeans, Couro, Tecido Sintético

#### Medidas
- **Medida**: 35cm, 36cm, 37cm, 38cm... (incrementos de 1cm)

## Restrição Importante de Edição

> **Atenção**: Observe o aviso exibido no sistema: "Após a criação da variante, não será possível excluir nem modificar. Só será possível adicionar valores a ela."

Essa limitação significa que:
- Uma vez criada, a variante não pode ser renomeada
- Os valores adicionados não podem ser excluídos
- Apenas novos valores podem ser incluídos posteriormente

## Finalizando o Cadastro

Após adicionar todos os valores desejados:

1. Revise cuidadosamente a lista de valores
2. Certifique-se de que não há erros de digitação ou valores ausentes
3. Clique no botão **Criar Variante** para finalizar
4. A variante será adicionada ao item e aparecerá na seção "Variantes do Item"

## Exemplos Práticos

### Exemplo 1: Variante de Tamanho para Vestuário

1. Selecione a aba **Vestuário**
2. Escolha **Tamanho (Vestuário)**
3. Nomeie a variante como "Tamanho"
4. Ative a opção **Variante Obrigatória**
5. Adicione os valores: PP, P, M, G, GG, XG
6. Clique em **Criar Variante**

### Exemplo 2: Variante de Cor para Protetor Auditivo

1. Selecione a aba **Cores**
2. Escolha **Cor (Básicas)**
3. Nomeie a variante como "Cor"
4. Deixe a opção **Variante Obrigatória** desativada
5. Adicione os valores: Preto, Branco, Cinza
6. Clique em **Criar Variante**

## Visualização das Variantes Configuradas

Após a criação bem-sucedida, a variante será exibida na tela de detalhes do item:

- Nome da variante (por exemplo, "Tamanho")
- Indicação se é obrigatória
- Lista de valores disponíveis organizados em cartões
- Botão para adicionar novas variantes

## Implicações no Estoque

Cada combinação de valores de variantes:
- Representa uma versão específica do item
- Possui seu próprio controle de estoque
- Será contabilizada separadamente nos relatórios
- Precisará ser especificada durante solicitações de EPI

## Próximos Passos

Após adicionar valores às variantes, você pode:

- [Configurar tipos adicionais de variante](./configurar-tipos-variante.md) para o mesmo item
- [Adicionar lotes ao estoque](../lotes/adicionar-lote.md) especificando as variantes
- [Verificar o inventário detalhado](../relatorios/estoque-atual.md) com as novas configurações
- [Editar variantes existentes](./editar-variantes.md) adicionando novos valores se necessário

---

*Última atualização: 18 de Maio de 2025*