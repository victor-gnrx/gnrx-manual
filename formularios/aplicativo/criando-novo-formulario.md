# Criando um Novo Formulário

A criação de um novo formulário permite instanciar um modelo pré-configurado para uma unidade específica de trabalho.

## Iniciando a Criação

### Acesso

1. Na tela Formulários, toque no botão "Novo"
2. Selecione "Novo Formulário" no menu
3. Aguarde o carregamento da tela de configuração

### Pré-requisitos

* Conexão com internet para carregar modelos (Caso não sincrozado)
* Permissões para criar formulários na unidade

## Campos de Configuração

### Modelo (Obrigatório)

* **Campo**: Dropdown "Selecione um modelo"
* **Função**: Define a estrutura base do formulário
* **Conteúdo**: Modelos disponíveis conforme suas permissões

### Unidade (Obrigatório)

* **Campo**: Dropdown para seleção de unidade
* **Função**: Define local de trabalho associado
* **Conteúdo**: Unidades que você tem acesso

### Nome do Formulário (Obrigatório - Gera Automaticamente)

* Padrão: \[DDMMYYYY] - \[NOME DO MODELO FORMULARIO] -  \[LOCAL]
* **Campo**: Campo de texto livre
* **Função**: Identificação do formulário
* **Formato**: Texto descritivo

### Descrição (Opcional)

* **Campo**: Campo de texto expandido
* **Função**: Informações adicionais sobre o formulário
* **Uso**: Contexto e instruções

## Seleção de Modelo

### Interface

* Modal com lista de modelos disponíveis
* Scroll vertical para navegar
* Toque no modelo para selecionar
* Botão X para fechar sem selecionar

### Conteúdo

* Nome do modelo
* Código de identificação
* Descrição resumida

## Seleção de Unidade

### Interface

* Modal com lista de unidades disponíveis
* Opções conforme permissões do usuário
* Seleção única obrigatória

### Impacto

* Define dados globais específicos
* Determina permissões de acesso
* Influencia relatórios e agrupamentos

## Finalização

### Botões de Ação

* **Cancelar**: Retorna sem salvar
* **Criar Formulário**: Confirma criação e abre formulário

### Validações

* Todos os campos obrigatórios preenchidos
* Modelo válido selecionado
* Unidade com permissão de acesso

### Resultado

* Formulário criado com status Ativo
* Redirecionamento para tela de detalhes
* Disponível para preenchimento
