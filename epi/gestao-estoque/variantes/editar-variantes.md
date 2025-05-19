# Editar Variantes

Esta página explica as possibilidades e limitações de edição de variantes de itens de EPI no Sistema GNRX Gestão de EPI.

## Visão Geral

O Sistema GNRX impõe restrições importantes na edição de variantes após sua criação inicial. Estas limitações visam garantir a integridade dos dados e a rastreabilidade do estoque ao longo do tempo. Esta página detalha o que pode e o que não pode ser alterado nas variantes existentes.

![Editar Variantes](../../../assets/images/editar-variantes.png)

## Aviso Importante

> **"Após a criação da variante, não será possível excluir nem modificar. Só será possível adicionar valores a ela."**

Esta restrição é claramente informada durante o processo de criação de variantes e deve ser considerada cuidadosamente ao configurar um novo item.

## O Que NÃO Pode Ser Editado

Após a criação de uma variante, os seguintes elementos NÃO podem ser modificados:

- **Nome da variante**: Uma vez definido como "Tamanho", "Cor", etc., não pode ser alterado
- **Obrigatoriedade**: Não é possível mudar uma variante de obrigatória para opcional, ou vice-versa
- **Valores existentes**: Não é possível excluir ou renomear valores já adicionados
- **Tipo de variante**: Não é possível converter um tipo de variante em outro

## O Que PODE Ser Editado

As únicas alterações permitidas são:

- **Adicionar novos valores**: É possível incluir valores adicionais a uma variante existente
- **Ordem de exibição**: Em alguns casos, é possível reorganizar a ordem de exibição dos valores

## Como Adicionar Novos Valores

Para adicionar um novo valor a uma variante existente:

1. Acesse o módulo **Inventário**
2. Clique no item desejado na lista para abrir seus detalhes
3. Navegue até a aba **Informações Item**
4. Na seção "Variantes do Item", localize a variante que deseja editar
5. Clique na variante para ver suas opções
6. Utilize a função de adicionar valor
7. Insira o novo valor e confirme

## Visualização das Variantes Configuradas

Após a criação, as variantes são exibidas como:

- Nome da variante (por exemplo, "Tamanho")
- Indicação se é obrigatória
- Lista de valores disponíveis
- A interface mostra claramente os valores já configurados

## Alternativas para Erros de Configuração

Caso tenha cometido um erro na criação da variante, suas opções são:

1. **Adicionar valores corretos**: Mantenha os valores incorretos e adicione os corretos para uso futuro
2. **Não utilizar os valores incorretos**: Simplesmente evite selecionar os valores errados ao adicionar estoque
3. **Desativar o item**: Em casos extremos, desative o item e crie um novo com a configuração correta

## Planejamento para Evitar Problemas

Devido às limitações de edição, é crucial:

1. **Planejar cuidadosamente**: Defina todas as variantes necessárias antes de criar
2. **Revisar antes de salvar**: Verifique todos os valores antes de finalizar a criação
3. **Considerar necessidades futuras**: Adicione valores que possam ser necessários no futuro
4. **Padronizar nomenclatura**: Use termos consistentes em todo o sistema

## Implicações no Estoque e Relatórios

É importante compreender que:

- Mesmo valores não utilizados continuarão aparecendo nas opções
- Relatórios incluirão todos os valores configurados
- O sistema não distingue entre valores ativos ou obsoletos

## Exemplos Práticos

### Exemplo 1: Adicionar um Novo Tamanho

Se você configurou uma variante "Tamanho" com valores P, M, G e posteriormente precisa adicionar XG:

1. Acesse a variante "Tamanho" do item
2. Utilize a função de adicionar valor
3. Insira "XG" como novo valor
4. Salve a alteração

### Exemplo 2: Correção de Erro de Configuração

Se configurou "Cor" com valores "Preta", "Branca", "Cinsa" (erro de digitação):

1. Não é possível excluir ou corrigir "Cinsa"
2. Adicione o valor correto "Cinza"
3. Ao adicionar estoque, utilize apenas o valor correto
4. O valor com erro permanecerá visível mas pode ser ignorado

## Próximos Passos

Após entender as limitações de edição de variantes, você pode:

- Revisar as [variantes configuradas](./configurar-tipos-variante.md) para seus itens
- Adicionar [novos valores](./adicionar-valores-variante.md) quando necessário
- Planejar cuidadosamente antes de [adicionar novas variantes](./configurar-tipos-variante.md)
- Gerenciar o [estoque específico](../lotes/adicionar-lote.md) para cada combinação de variantes

---

*Última atualização: 18 de Maio de 2025*