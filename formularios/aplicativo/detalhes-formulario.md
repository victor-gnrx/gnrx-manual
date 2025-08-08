# Detalhes do Formulário

A tela de detalhes apresenta informações completas do formulário, incluindo cabeçalho, registros e dados globais organizados em seções expansíveis.

## Cabeçalho do Formulário

### Informações Principais

* **Nome**: Nome do Formulário
* **Modelo**: Tipo de modelo utilizado como base
* **Unidade**: Local de trabalho associado

### Status e Controles

* **Status**: Ativo e Concluído
* **Tipo**: Categoria do formulário (Padrão apenas)
* **IDs de Controle**: ID Local (Identificador único no dispositivo) e ID Server (Identificador único no servidor - já sincronizado)

## Seções do Formulário

### Dados Globais

* **Função**: Informações compartilhadas entre registros
* **Edição**: Sempre possível, exceto assinatura.
* **Estados**: Obrigatório ou opcional

### Registros

* **Função**: Lista de todos os registros do formulário
* **Contagem**: Número total entre parênteses
* **Pesquisa**: Campo para filtrar registros
* **Adição**: Botão "+" para novo registro

## Interface de Registros

### Lista de Registros

* **Colunas**: Sincronização, Opções, Data, campos do modelo
* **Status**: Indicadores visuais de sincronização
* **Ações**: Menu de opções por registro
* **Ordenação**: Por data ou outros critérios

### Estados dos Registros

* **Sincronizado**: Dados no servidor
* **Pendente**: Aguardando upload
* **Falha**: Erro na sincronização
* **Rascunho**: Em preenchimento

## Navegação e Ações

### Botão de Voltar

* **Função**: Retorna à lista de formulários
* **Localização**: Canto superior esquerdo

<figure><img src="../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>

### Menu de Ações

* **Função**: Ações específicas do formulário
* **Localização**: Canto superior direito
* **Conteúdo**: Concluir Formulário

<figure><img src="../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

### Ações nos Registros

* **Visualizar**: Ver detalhes do registro
* **Editar**: Modificar dados (se em rascunho / registro padrão)

## Sincronização

<figure><img src="../.gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure>

### Status Visual

* **Cores**: GNRx (sincronizado), Amarelo (pendente), Vermelho (falha), Nude (Rascunho)
* **Ícones**: Indicadores específicos por estado
* **Texto**: Descrição do status atual
