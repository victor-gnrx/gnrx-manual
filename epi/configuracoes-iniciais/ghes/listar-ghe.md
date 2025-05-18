# Listar GHEs

Esta página explica como acessar, visualizar e filtrar a lista de Grupos Homogêneos de Exposição (GHEs) cadastrados no Sistema GNRX Gestão de EPI.

## Acessando a Lista de GHEs

Para acessar a lista de GHEs cadastrados no sistema:

1. No menu lateral, clique em **Estruturas**
2. Selecione **GHEs**

![Acesso à Lista de GHEs](../../../assets/images/acesso-ghes.png)

## Interface da Lista de GHEs

A tela de listagem de GHEs apresenta uma visão consolidada de todos os grupos cadastrados no sistema:

![Lista de GHEs](../../../assets/images/lista-ghes.png)

### Elementos da Interface

1. **Cabeçalho**:
   - **Total de GHEs**: Contador do número de grupos ativos
   - **Botão "Novo GHE"**: Para adicionar um novo grupo ao sistema

2. **Barra de Pesquisa**:
   - Campo para busca de GHEs por nome ou ID
   - Botão "Pesquisar" para iniciar a busca

3. **Tabela de GHEs**:
   - **ID**: Identificador único do GHE
   - **Nome**: Nome do grupo
   - **Unidade**: Unidade física vinculada ao GHE
   - **Descrição**: Informações adicionais sobre o grupo
   - **Situação**: Estado atual (Ativo/Inativo)
   - **Criado em**: Data de criação do registro
   - **Atualizado em**: Data da última modificação
   - **Opções**: Botões de ação (visualizar, editar, excluir)

## Funcionalidades Disponíveis

### Pesquisa e Filtros

Para localizar GHEs específicos:

1. Digite um termo de busca no campo de pesquisa (nome, ID ou parte da descrição)
2. Clique no botão **Pesquisar**
3. O sistema exibirá apenas os GHEs que correspondem aos critérios de busca

> **Dica:** Para filtrar GHEs por unidade específica, digite o nome da unidade no campo de pesquisa.

### Ações por GHE

Para cada GHE na lista, você pode executar as seguintes ações através dos botões na coluna "Opções":

![Botões de Ação](../../../assets/images/botoes-acao-ghes.png)

- **Visualizar** (ícone de olho): Abre a tela de detalhes do GHE
- **Editar** (ícone de lápis): Abre o formulário para edição dos dados
- **Excluir/Desativar** (ícone de lixeira): Inicia o processo de desativação do GHE

### Exportação da Lista

Para exportar a lista de GHEs:

1. Localize o ícone de exportação no canto superior direito da tabela
2. Clique no ícone para abrir as opções de exportação
3. Selecione o formato desejado (Excel, CSV ou PDF)
4. O sistema gerará o arquivo para download

## Navegação para Detalhes

Para visualizar informações detalhadas de um GHE específico:

1. Clique no nome do GHE na lista ou no ícone de visualização (olho)
2. O sistema abrirá a tela de detalhes do GHE, com abas para:
   - **Visão Geral**: Informações básicas
   - **Riscos / EPIs**: Riscos associados e equipamentos de proteção

![Navegação para Detalhes](../../../assets/images/navegacao-detalhes-ghe.png)

## Ordenação da Lista

A lista de GHEs pode ser ordenada por qualquer uma das colunas:

1. Clique no cabeçalho da coluna desejada
2. Um pequeno ícone de seta indicará a direção da ordenação (ascendente/descendente)
3. Clique novamente no mesmo cabeçalho para inverter a ordem

## Agrupamento por Unidades

Observe que os GHEs são agrupados por unidade, o que significa que:

- É possível ter GHEs com mesmo nome em unidades diferentes
- O mesmo conceito de grupo pode ser replicado em cada unidade física
- A identificação completa de um GHE inclui sempre seu nome e unidade

No exemplo da lista, é possível observar "ghe 01" e "ghe 02" presentes em ambas as unidades "Belo Horizonte" e "Belo Horizonte 2".

## Visualização de Situação

Os GHEs na lista são apresentados com indicadores visuais de situação:

- **Ativo**: Exibido em verde, indica GHE em operação normal
- **Inativo**: Exibido em vermelho, indica GHE temporariamente desativado

## Datas de Criação e Atualização

As colunas de datas fornecem informações importantes para auditoria:

- **Criado em**: Indica quando o GHE foi originalmente cadastrado
- **Atualizado em**: Mostra a data da última modificação realizada

Estas informações são úteis para verificação de conformidade e histórico de alterações.

## Solução de Problemas Comuns

| Problema | Solução |
|----------|---------|
| Lista de GHEs vazia | Verifique se você tem permissões para visualizar GHEs ou se ainda não há grupos cadastrados no sistema |
| Pesquisa não retorna resultados | Tente termos mais genéricos ou verifique a ortografia |
| GHE não aparece para unidade específica | Verifique se o GHE foi criado para a unidade correta |

## Próximos Passos

Após visualizar a lista de GHEs, você pode:

- [Criar um novo GHE](./criar-ghe.md)
- [Editar um GHE existente](./editar-ghe.md)
- [Desativar um GHE](./desativar-ghe.md)
- Ver detalhes de um GHE específico para [vincular riscos](./vincular-riscos.md) ou [vincular EPIs](./vincular-epis.md)
- Associar [colaboradores](../colaboradores/README.md) aos GHEs adequados

---

*Última atualização: 16 de Maio de 2025*