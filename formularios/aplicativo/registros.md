# Registros

Os registros representam as coletas de dados individuais dentro de um formulário, seguindo a estrutura definida pelo modelo selecionado.

<figure><img src="../.gitbook/assets/image (5).png" alt="" width="224"><figcaption></figcaption></figure>

## Visualizando Registros

### Lista de Registros

* **Tabela organizada**: Colunas com informações principais
* **Status de sincronização**: Indicador visual por linha
* **Campo de pesquisa**: Filtro em tempo real
* **Contagem total**: Número de registros entre parênteses

### Colunas Exibidas

* **Sinc.**: Status de sincronização
* **Opções**: Menu de ações do registro
* **Campos do modelo**: Conforme configuração

## Criando Novo Registro

Para criar um novo registro, é necessário seguir os passos abaixo. Caso a opção não exista, o modelo não permite a adição de novos registros ou o formulário já foi concluído.

### Iniciando Preenchimento&#x20;

1. Vá até a secão que quer adicionar registros. Se não tiver seção, utilize a principal, "Registros".
2. Toque no botão "+" na seção de registros
3. Acesse a tela de preenchimento
4. Complete os campos obrigatórios
5. Clique em "Salvar"

<figure><img src="../.gitbook/assets/image (8).png" alt=""><figcaption></figcaption></figure>



## Preenchimento de Campos

### Tipos de Campos

#### Campo de Data

* **Interface**: Seletor de calendário
* **Marcação**: Asterisco (\*) se obrigatório
* **Validação**: Formato de data automático

<figure><img src="../.gitbook/assets/image (13).png" alt=""><figcaption></figcaption></figure>

#### Campo de Hora

* **Interface**: Seletor de hora
* **Marcação**: Asterisco (\*) se obrigatório
* **Validação**: Formato de data automático

<figure><img src="../.gitbook/assets/image (11).png" alt=""><figcaption></figcaption></figure>

#### Campo de Seleção única / múltipla

* **Interface**: Dropdown com opções
* **Conteúdo**: Opções pré-definidas no modelo
* **Validação**: Seleção obrigatória se marcado

<figure><img src="../.gitbook/assets/image (9).png" alt=""><figcaption></figcaption></figure>

#### Campo de Texto

* **Interface**: Caixa de texto livre
* **Validação**: Apenas obrigatoriedade
* **Formato**: Texto livre

<figure><img src="../.gitbook/assets/image (12).png" alt=""><figcaption></figcaption></figure>

#### Campo Numérico

* **Interface**: Teclado numérico
* **Validação**: Apenas números aceitos
* **Formato**: Apenas números

<figure><img src="../.gitbook/assets/image (12).png" alt=""><figcaption></figcaption></figure>

Campo Foto

* Interface: Botão para anexar fotos
* Validacão: Apenas obrigatoriedade

Campo Assinatura

* Interface: Botão de assinatura
* Validacão: Apenas obrigatoriedade
* Formato: Campo para escrita da assinatura

<figure><img src="../.gitbook/assets/image (14).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (15).png" alt=""><figcaption></figcaption></figure>

Campo Temperatura

* Interface: Teclado numérico
* Validação: Apenas temperaturas válidas
* Formato: Temperatura com ºC

<figure><img src="../.gitbook/assets/image (10).png" alt=""><figcaption></figcaption></figure>



### Validações em Tempo Real

* **Campos obrigatórios**: Indicados com asterisco (\*)
* **Mensagens de erro**: Feedback imediato
* **Bloqueio de salvamento completo**: Até correção de erros

## Estados dos Registros

### Rascunho

* **Significado**: Preenchimento em andamento
* **Cor**: Indicador específico
* **Ações**: Continuar preenchimento

### Pendente

* **Significado**: Aguardando sincronização
* **Cor**: Amarelo
* **Ações**: Visualizar

### Sincronizado

* **Significado**: Dados no servidor
* **Cor**: Verde
* **Ações**: Visualizar, editar (se permitido)

### Falha

* **Significado**: Erro na sincronização
* **Cor**: Vermelho
* **Ações**: Visualizar

## Gerenciamento de Registros

### Ações Disponíveis

* **Visualizar**: Ver dados completos
* **Editar**: Modificar informações (se rascunho)

### Ordenação

* **Por data**: Mais recentes primeiro (padrão)

## Trabalho Offline

### Preenchimento Sem Conexão

* **Funcionalidade completa**: Todos os campos funcionam
* **Salvamento local**: Dados seguros no dispositivo
* **Validações**: Funcionam normalmente offline
* **Sincronização posterior**: Automátia ao concluir e/ou forçando sincronização na tela de configurações

### Indicadores Offline

* **Status visual**: Indicação de dados não sincronizados
* **Backup local**: Proteção contra perda
* **Queue de sincronização**: Ordem de envio quando conectar

## Resolução de Problemas

### Registro Não Salva

* **Verificar campos obrigatórios**: Completar todos os asteriscos
* **Validar formatos**: Conferir datas, números
* **Verificar espaço**: Memória disponível no dispositivo

### Erro de Sincronização

* **Verificar conexão**: Internet estável
* **Tentar novamente**: Após alguns minutos
* **Verificar dados**: Formatos e valores válidos
* Verificar Log de erros na tela de configuracões

