# Listar Setores

Esta página explica como acessar, visualizar e filtrar a lista de setores cadastrados no Sistema GNRX Gestão de EPI.

## Acessando a Lista de Setores

Para acessar a lista de setores cadastrados no sistema:

1. No menu lateral, clique em **Estruturas**
2. Selecione **Setores**

![Acesso à Lista de Setores](../../../assets/images/acesso-setores.png)

## Interface da Lista de Setores

A tela de listagem de setores apresenta uma visão consolidada de todos os setores cadastrados no sistema:

![Lista de Setores](../../../assets/images/lista-setores.png)

### Elementos da Interface

1. **Cabeçalho**:
   - **Total de setores**: Contador do número de setores ativos
   - **Botão "Novo Setor"**: Para adicionar um novo setor ao sistema

2. **Barra de Pesquisa**:
   - Campo para busca de setores por nome ou ID
   - Botão "Pesquisar" para iniciar a busca

3. **Tabela de Setores**:
   - **ID**: Identificador único do setor
   - **Nome**: Nome do setor
   - **Descrição**: Informações adicionais sobre o setor
   - **Situação**: Estado atual (Ativo/Inativo)
   - **Opções**: Botões de ação (visualizar, editar, excluir)

## Funcionalidades Disponíveis

### Pesquisa e Filtros

Para localizar setores específicos:

1. Digite um termo de busca no campo de pesquisa (nome ou ID)
2. Clique no botão **Pesquisar**
3. O sistema exibirá apenas os setores que correspondem aos critérios de busca

> **Dica:** Para retornar à lista completa, limpe o campo de pesquisa e clique novamente em Pesquisar.

### Ações por Setor

Para cada setor na lista, você pode executar as seguintes ações através dos botões na coluna "Opções":

![Botões de Ação](../../../assets/images/botoes-acao-setores.png)

- **Visualizar** (ícone de olho): Abre a tela de detalhes do setor
- **Editar** (ícone de lápis): Abre o formulário para edição dos dados
- **Excluir/Desativar** (ícone de lixeira): Inicia o processo de desativação do setor

### Exportação da Lista

Para exportar a lista de setores:

1. Localize o ícone de exportação no canto superior direito da tabela
2. Clique no ícone para gerar um arquivo no formato desejado (Excel, CSV ou PDF)
3. O sistema processará a solicitação e iniciará o download automaticamente

## Navegação para Detalhes

Para visualizar informações detalhadas de um setor específico:

1. Clique no nome do setor na lista ou no ícone de visualização (olho)
2. O sistema abrirá a tela de detalhes do setor, com abas para:
   - **Visão Geral**: Informações básicas e estatísticas
   - **Unidades**: Lista de unidades onde o setor está presente
   - **Colaboradores**: Funcionários associados ao setor
   - **Estatísticas**: Dados analíticos sobre o setor

![Detalhes do Setor](../../../assets/images/detalhes-setor.png)

## Ordenação da Lista

A lista de setores pode ser ordenada por qualquer uma das colunas:

1. Clique no cabeçalho da coluna desejada
2. Um pequeno ícone de seta indicará a direção da ordenação (ascendente/descendente)
3. Clique novamente no mesmo cabeçalho para inverter a ordem

## Visualização de Situação

Os setores na lista são apresentados com indicadores visuais de situação:

- **Ativo**: Exibido em verde, indica setor em operação normal
- **Inativo**: Exibido em vermelho, indica setor temporariamente desativado

> **Nota:** Setores inativos não aparecem em listas de seleção em outros módulos do sistema, mas mantêm seu histórico preservado.

## Navegação Entre Páginas

Se houver muitos setores, a lista será dividida em múltiplas páginas:

1. No rodapé da tabela, são exibidos controles de paginação
2. Utilize as setas ou números de página para navegar
3. É possível também ajustar o número de itens por página através do seletor

## Filtro por Situação

Para visualizar setores inativos junto com os ativos:

1. Localize o filtro de situação próximo à barra de pesquisa
2. Marque a opção "Mostrar Inativos"
3. A lista será atualizada para incluir todos os setores, independente da situação

## Solução de Problemas Comuns

| Problema | Solução |
|----------|---------|
| Lista de setores vazia | Verifique se você tem permissões para visualizar setores ou se ainda não há setores cadastrados no sistema |
| Pesquisa não retorna resultados | Tente termos mais genéricos ou verifique a ortografia |
| Setor não pode ser excluído | Verifique se há colaboradores ou GHEs associados ao setor |

## Próximos Passos

Após visualizar a lista de setores, você pode:

- [Criar um novo setor](./criar-setor.md)
- [Editar um setor existente](./editar-setor.md)
- [Desativar um setor](./desativar-setor.md)
- [Vincular unidades a um setor](./vincular-unidades.md)
- Associar [colaboradores](../colaboradores/README.md) aos setores

---

*Última atualização: 16 de Maio de 2025*