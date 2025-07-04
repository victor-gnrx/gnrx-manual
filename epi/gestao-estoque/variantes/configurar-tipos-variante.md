---
icon: paintbrush-fine
---

# Configurar Tipos de Variante

Esta página explica como configurar tipos de variante para itens de EPI no Sistema GNRX Gestão de EPI.

## Visão Geral

As variantes permitem gerenciar diferentes características de um mesmo item de EPI, como tamanhos, cores, modelos ou outras especificações relevantes. Esta funcionalidade é essencial para o controle preciso do estoque e para garantir que cada colaborador receba o equipamento adequado às suas necessidades.

![Configurar Tipos de Variante](<../../.gitbook/assets/image (34).png>)

## Acesso à Configuração de Variantes

Para configurar variantes de um item:

1. Acesse o módulo **Inventário**
2. Clique no item desejado na lista para abrir seus detalhes
3. Navegue até a aba **Informações Item**
4. Na seção "Variantes do Item", clique no botão **Adicionar Variante**

## Quando Utilizar Variantes

As variantes são úteis para itens que possuem:

* Diferentes tamanhos (P, M, G, XG, etc.)
* Diversas cores disponíveis
* Modelos específicos do mesmo tipo de EPI
* Características que afetam a compatibilidade com o usuário
* Versões para uso em diferentes ambientes

## Utilizando Categorias Pré-configuradas

O sistema oferece categorias pré-configuradas para facilitar o cadastro:

1. **Vestuário**: Para uniformes e roupas de proteção
   * Tamanho (Vestuário): PP, P, M, G, GG, XG
   * Tamanho (Infantil): 2, 4, 6, 8, 10, 12, 14, 16
2. **Calçados**: Para botas e sapatos de segurança
   * Tamanho (Calçado): 32, 33, 34, 35... até 44
3. **Cores**: Divididas em dois grupos
   * Cor (Básicas): Preto, Branco, Cinza, Bege, Marrom
   * Cor (Vibrantes): Vermelho, Azul, Verde, Amarelo, Roxo, Rosa, Laranja
4. **Materiais**: Composição do item
   * Material: Algodão, Poliéster, Nylon, Linho, Jeans, Couro, etc.
5. **Medidas**: Dimensões em centímetros
   * Medida: 35cm, 36cm, 37cm, etc.

## Criando uma Nova Variante

Para criar uma variante personalizada:

1. Clique na categoria apropriada (Vestuário, Calçados, Cores, etc.)
2. Selecione o sub-tipo se disponível (ex: Tamanho (Vestuário) ou Tamanho (Infantil))
3. Defina o **Nome da Variante** (ex: "Tamanho", "Cor", "Modelo")
4. Decida se a variante será **Obrigatória** ativando ou não o toggle
5. Note o aviso importante: **"Após a criação da variante, não será possível excluir nem modificar. Só será possível adicionar valores a ela."**
6. Adicione os **Valores da Variante** utilizando o botão "+ Adicionar"
7. Clique em **Criar Variante** para finalizar

## Valores Pré-definidos por Categoria

Cada categoria tem valores pré-configurados que podem ser utilizados:

### Vestuário

* Tamanho (Vestuário): PP, P, M, G, GG, XG
* Tamanho (Infantil): 2, 4, 6, 8, 10, 12, 14, 16

### Calçados

* Tamanho (Calçado): 32, 33, 34, 35, 36, 37, 38, 39, 40, 41, 42, 43, 44

### Cores

* Cor (Básicas): Preto, Branco, Cinza, Bege, Marrom
* Cor (Vibrantes): Vermelho, Azul, Verde, Amarelo, Roxo, Rosa, Laranja

### Materiais

* Material: Algodão, Poliéster, Nylon, Linho, Jeans, Couro, Tecido Sintético

### Medidas

* Medida: 35cm, 36cm, 37cm até 54cm (incrementos de 1cm)

## Exemplos de Uso

### Para um Protetor Auditivo

1. Adicione a variante "Tamanho" com valores:
   * "Único"
   * "Ajustável"

### Para um Uniforme

1. Adicione a variante "Tamanho" com valores do Vestuário (PP até XG)
2. Adicione a variante "Cor" com as cores disponíveis

### Para um Capacete de Segurança

1. Adicione a variante "Tamanho" com valores específicos
2. Adicione a variante "Cor" com as opções disponíveis
3. Adicione a variante "Material" se aplicável

## Implicações no Estoque

Ao configurar variantes:

* O sistema criará combinações das diferentes variantes
* Cada combinação terá seu próprio controle de estoque
* Os lotes deverão especificar quais variantes contêm
* A rastreabilidade será mantida por combinação específica

## Visualização das Variantes Configuradas

Após a criação, as variantes aparecerão na seção "Variantes do Item" com:

* Nome da variante
* Valores disponíveis
* Indicação se é obrigatória
* Opção para adicionar mais variantes

## Limitações e Considerações Importantes

* Uma vez criada, uma variante **não pode ser modificada ou excluída**
* Apenas novos valores podem ser adicionados a uma variante existente
* O planejamento cuidadoso antes da criação é essencial
* Múltiplas variantes aumentam exponencialmente as combinações possíveis

## Próximos Passos

Após configurar os tipos de variante, você pode:

* [Adicionar valores às variantes](adicionar-valores-variante.md)
* [Adicionar lotes com variantes específicas](../lotes/adicionar-lote.md)
* [Verificar o inventário detalhado](../relatorios/estoque-atual.md) com as variantes configuradas

***

_Última atualização: 18 de Maio de 2025_
