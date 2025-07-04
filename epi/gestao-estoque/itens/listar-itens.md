# Listar Itens

Esta página explica como visualizar e gerenciar a lista de itens de EPI cadastrados no Sistema GNRX Gestão de EPI.

## Visão Geral

A tela de listagem de itens é o ponto central do módulo de Gestão de Estoque, permitindo visualizar todos os Equipamentos de Proteção Individual cadastrados no sistema, com suas informações essenciais como número de CA, validade, fabricante e quantidade em estoque.

<figure><img src="../../.gitbook/assets/image (27).png" alt=""><figcaption></figcaption></figure>

## Acessando a Lista de Itens

Para acessar a lista de itens:

1. No menu lateral, clique em **Inventário**
2. Selecione **Inventário de Items**

Alternativamente, você pode clicar diretamente em **Controle de Inventário** no menu lateral, se disponível.

## Interface da Lista de Itens

A tela de listagem de itens apresenta os seguintes elementos:

### Cabeçalho

* **Inventário de Items**: Título da página
* **Total de items cadastrados**: Contador que exibe o número total de tipos de EPIs no sistema
* **Novo Item**: Botão para adicionar um novo EPI
* **Exportar PDF**: Botão para gerar relatório em PDF do inventário

### Ferramentas de Pesquisa e Filtros

* **Campo de pesquisa**: Para buscar itens por nome, CA ou outras informações
* **Botão Pesquisar**: Para executar a busca
* **Predefinições de Período**: Atalho para filtros de período de troca

### Tabela de Itens

A tabela exibe os itens com as seguintes colunas:

* **ID**: Identificador único do item no sistema
* **Nome**: Nome do EPI conforme cadastrado
* **CA**: Número do Certificado de Aprovação (quando aplicável)
* **Validade até**: Data de validade do CA
* **Fabricante**: Fabricante ou fornecedor
* **Tempo de Troca**: Período recomendado para substituição (em dias)
* **Estoque**: Quantidade disponível com link para detalhes
* **Situação**: Status atual (Ativo/Inativo)
* **Opções**: Botões de ação para visualizar, editar ou excluir

## Visualizando Detalhes do Estoque

Os números na coluna "Estoque" funcionam como links:

1. Clique no número com o ícone ao lado (ex: "195 itens")
2. O sistema abrirá a tela de detalhes do inventário para aquele item específico
3. Você poderá ver informações adicionais como itens em uso, disponíveis e totais

## Funcionalidades Principais

### Pesquisa de Itens

Para localizar itens específicos:

1. Digite termos de busca no campo "Pesquisar items..."
2. Você pode pesquisar por:
   * Nome do item
   * Número do CA
   * Fabricante
   * Qualquer texto contido nas informações do item
3. Clique no botão "Pesquisar" ou pressione Enter

### Filtros por Unidade

Para visualizar itens de uma unidade específica:

1. No canto superior direito, utilize o seletor de unidade (ex: "Belo Horizonte 2")
2. A lista será atualizada automaticamente para mostrar apenas os itens daquela unidade

### Predefinições de Período

Para acessar as predefinições de período de troca:

1. Clique no botão "Predefinições de Período" no canto superior direito
2. O sistema exibirá as predefinições existentes ou a opção de criar novas

### Ordenação da Lista

Para ordenar a lista por diferentes critérios:

1. Clique no cabeçalho da coluna desejada (Nome, CA, Validade, etc.)
2. Clique novamente para alternar entre ordem crescente e decrescente

## Ações por Item

Para cada item na lista, você tem as seguintes opções:

* **Visualizar** (ícone de olho): Abre a tela de detalhes do item
* **Editar** (ícone de lápis): Abre o formulário para edição do item
* **Excluir/Inativar** (ícone de lixeira): Inativa o item (não disponível para itens em uso)

## Exportação do Inventário

Para exportar a lista de itens em formato PDF:

1. Clique no botão "Exportar PDF" no canto superior direito
2. Selecione o tipo de relatório desejado:
   * **Resumido**: Apenas informações básicas dos itens
   * **Variações**: Inclui detalhes sobre as variantes de cada item
   * **Completo**: Relatório detalhado com todas as informações
3. O sistema irá gerar o PDF e iniciar o download automaticamente

<figure><img src="../../.gitbook/assets/image (28).png" alt=""><figcaption><p>Exportar relatório</p></figcaption></figure>

## Significado das Informações

### Tempo de Troca

* Indica o período recomendado (em dias) para substituição do EPI
* "0 dias" significa que não há período definido
* Itens sem CA (como uniformes) geralmente não têm tempo de troca obrigatório

### Situação

* **Ativo**: Item disponível para uso e solicitações
* **Inativo**: Item desativado (não aparece em novas solicitações)

### Estoque

* Exibe a quantidade total disponível
* Os números são clicáveis e levam aos detalhes do inventário

## Itens Sem CA

Itens sem Certificado de Aprovação (CA) são identificados por:

* "N/A" no campo de CA
* "N/A" no campo de validade
* Geralmente representam uniformes ou acessórios complementares

## Próximos Passos

A partir da lista de itens, você pode:

* [Criar um novo item com CA](criar-item-com-ca.md)
* [Criar um novo item sem CA](criar-item-sem-ca.md)
* [Editar um item existente](editar-item.md)
* [Gerenciar lotes e estoque](../lotes/)

***

_Última atualização: 18 de Maio de 2025_
