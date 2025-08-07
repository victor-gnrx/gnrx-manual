# Registros

Os registros representam as coletas de dados individuais dentro de um formulário, seguindo a estrutura definida pelo modelo selecionado.

## Visualizando Registros

### Lista de Registros
- **Tabela organizada**: Colunas com informações principais
- **Status de sincronização**: Indicador visual por linha
- **Campo de pesquisa**: Filtro em tempo real
- **Contagem total**: Número de registros entre parênteses

### Colunas Exibidas
- **Sinc.**: Status de sincronização
- **Opções**: Menu de ações do registro
- **Data**: Data do preenchimento
- **Campos do modelo**: Conforme configuração

## Criando Novo Registro

### Iniciando Preenchimento
1. Toque no botão "+" na seção de registros
2. Selecione "Concluir" no modal de ações
3. Acesse a tela de preenchimento
4. Complete os campos obrigatórios

### Modal de Ações
- **Opções disponíveis**: Conforme modelo configurado
- **Ação padrão**: Normalmente "Concluir"
- **Cancelamento**: Botão X para fechar

## Preenchimento de Campos

### Tipos de Campos

#### Campo de Data
- **Interface**: Seletor de calendário
- **Marcação**: Asterisco (*) se obrigatório
- **Validação**: Formato de data automático

#### Campo de Seleção
- **Interface**: Dropdown com opções
- **Conteúdo**: Opções pré-definidas no modelo
- **Validação**: Seleção obrigatória se marcado

#### Campo de Texto
- **Interface**: Caixa de texto livre
- **Validação**: Limite de caracteres se configurado
- **Formato**: Máscara automática se aplicável

#### Campo de Texto Longo
- **Interface**: Área de texto expandida
- **Uso**: Descrições, observações, evidências
- **Limite**: Conforme configuração do modelo

#### Campo Numérico
- **Interface**: Teclado numérico
- **Validação**: Apenas números aceitos
- **Formato**: Decimais conforme configuração

### Validações em Tempo Real
- **Campos obrigatórios**: Indicados com asterisco (*)
- **Formato**: Validação durante digitação
- **Mensagens de erro**: Feedback imediato
- **Bloqueio de envio**: Até correção de erros

## Estados dos Registros

### Rascunho
- **Significado**: Preenchimento em andamento
- **Cor**: Indicador específico
- **Ações**: Continuar preenchimento, excluir

### Pendente
- **Significado**: Aguardando sincronização
- **Cor**: Amarelo
- **Ações**: Visualizar, forçar sincronização

### Sincronizado
- **Significado**: Dados no servidor
- **Cor**: Verde
- **Ações**: Visualizar, editar (se permitido)

### Falha
- **Significado**: Erro na sincronização
- **Cor**: Vermelho
- **Ações**: Tentar novamente, verificar dados

## Gerenciamento de Registros

### Ações Disponíveis
- **Visualizar**: Ver dados completos
- **Editar**: Modificar informações (se permitido)
- **Excluir**: Remover registro (se permitido)
- **Duplicar**: Criar cópia com mesmo modelo

### Pesquisa de Registros
- **Campo de busca**: Localizado acima da lista
- **Busca em tempo real**: Filtro conforme digitação
- **Campos pesquisáveis**: Todos os campos visíveis
- **Limpar busca**: Remover filtro aplicado

### Ordenação
- **Por data**: Mais recentes primeiro (padrão)
- **Por status**: Agrupados por estado
- **Por campo**: Conforme colunas disponíveis

## Trabalho Offline

### Preenchimento Sem Conexão
- **Funcionalidade completa**: Todos os campos funcionam
- **Salvamento local**: Dados seguros no dispositivo
- **Validações**: Funcionam normalmente offline
- **Sincronização posterior**: Automática quando conectar

### Indicadores Offline
- **Status visual**: Indicação de dados não sincronizados
- **Backup local**: Proteção contra perda
- **Queue de sincronização**: Ordem de envio quando conectar

## Resolução de Problemas

### Registro Não Salva
- **Verificar campos obrigatórios**: Completar todos os asteriscos
- **Validar formatos**: Conferir datas, números
- **Verificar espaço**: Memória disponível no dispositivo

### Erro de Sincronização
- **Verificar conexão**: Internet estável
- **Tentar novamente**: Após alguns minutos
- **Verificar dados**: Formatos e valores válidos

### Registro Perdido
- **Verificar rascunhos**: Dados salvos automaticamente
- **Verificar filtros**: Pode estar oculto por pesquisa
- **Sincronizar**: Baixar dados do servidor