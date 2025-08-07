# Detalhes do Formulário

A tela de detalhes apresenta informações completas do formulário, incluindo cabeçalho, registros e dados globais organizados em seções expansíveis.

## Cabeçalho do Formulário

### Informações Principais
- **ID e Nome**: Identificação única do formulário
- **Modelo**: Tipo de modelo utilizado como base
- **Unidade**: Local de trabalho associado

### Status e Controles
- **Status**: Ativo, Inativo ou Padrão (indicado por cor)
- **Tipo**: Categoria do formulário
- **IDs de Controle**: ID Local e ID Server

### Indicadores de Sincronização
- **Sincronizado**: Dados atualizados no servidor
- **Pendente**: Aguardando sincronização
- **Falha**: Erro na sincronização
- **Não Sincronizado**: Apenas dados locais

## Seções do Formulário

### Dados Globais
- **Função**: Informações compartilhadas entre registros
- **Visualização**: Cards com chave, valor e tipo
- **Edição**: Disponível conforme permissões
- **Estados**: Obrigatório ou opcional

### Registros
- **Função**: Lista de todos os registros do formulário
- **Contagem**: Número total entre parênteses
- **Pesquisa**: Campo para filtrar registros
- **Adição**: Botão "+" para novo registro

## Interface de Registros

### Lista de Registros
- **Colunas**: Sincronização, Opções, Data, campos do modelo
- **Status**: Indicadores visuais de sincronização
- **Ações**: Menu de opções por registro
- **Ordenação**: Por data ou outros critérios

### Estados dos Registros
- **Sincronizado**: Dados no servidor
- **Pendente**: Aguardando upload
- **Falha**: Erro na sincronização
- **Rascunho**: Em preenchimento

## Navegação e Ações

### Botão de Voltar
- **Função**: Retorna à lista de formulários
- **Localização**: Canto superior esquerdo

### Menu de Ações
- **Função**: Ações específicas do formulário
- **Localização**: Canto superior direito
- **Conteúdo**: Conforme permissões do usuário

### Ações nos Registros
- **Visualizar**: Ver detalhes do registro
- **Editar**: Modificar dados (se permitido)
- **Excluir**: Remover registro (se permitido)
- **Sincronizar**: Forçar sincronização

## Pesquisa e Filtros

### Campo de Pesquisa
- **Localização**: Acima da lista de registros
- **Função**: Filtrar registros em tempo real
- **Escopo**: Busca em campos visíveis

### Filtros por Status
- **Todos**: Exibe todos os registros
- **Sincronizados**: Apenas registros no servidor
- **Pendentes**: Aguardando sincronização
- **Com erro**: Registros com falha

## Sincronização

### Status Visual
- **Cores**: Verde (ok), Amarelo (pendente), Vermelho (erro)
- **Ícones**: Indicadores específicos por estado
- **Texto**: Descrição do status atual

### Ações de Sincronização
- **Automática**: Quando há conexão disponível
- **Manual**: Puxar tela para baixo para atualizar
- **Individual**: Sincronizar registro específico