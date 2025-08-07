# Manual do Usuário - GNRx Formulários
## Aplicativo Mobile

---

## Índice

1. [Introdução](#introducao)
2. [Primeiros Passos](#primeiros-passos)
3. [Navegação Principal](#navegacao-principal)
4. [Meus Formulários](#meus-formularios)
5. [Criando um Novo Formulário](#criando-novo-formulario)
6. [Detalhes do Formulário](#detalhes-formulario)
7. [Registros](#registros)
8. [Estados e Status](#estados-status)
9. [Sincronização](#sincronizacao)
10. [Dicas e Boas Práticas](#dicas-boas-praticas)

---

## 1. Introdução {#introducao}

O **GNRx Formulários** é um aplicativo mobile que permite criar, gerenciar e preencher formulários personalizados diretamente do seu dispositivo móvel. O app funciona tanto online quanto offline, garantindo que você nunca perca dados importantes.

### Principais Funcionalidades

- ✅ Criação de formulários baseados em modelos
- ✅ Preenchimento offline com sincronização automática
- ✅ Diferentes tipos de campos (texto, data, seleção, etc.)
- ✅ Controle de status e validações
- ✅ Interface intuitiva e responsiva

---

## 2. Primeiros Passos {#primeiros-passos}

### Download e Instalação

O aplicativo está disponível na Google Play Store. Procure por **"GNRx - Forms"** ou acesse diretamente através do link fornecido pela sua empresa.

### Login

Após a instalação, faça login com as credenciais fornecidas pelo administrador do sistema da sua empresa.

---

## 3. Navegação Principal {#navegacao-principal}

O aplicativo possui uma barra de navegação inferior com três seções principais:

### 📋 Formulários
Visualize e gerencie todos os seus formulários

### 📄 Modelos  
Acesse os modelos disponíveis para criar novos formulários

### ⚙️ Configurações
Ajustes do aplicativo e configurações da conta

---

## 4. Meus Formulários {#meus-formularios}

Na tela principal "Formulários", você encontra todos os formulários da sua empresa organizados por status.

### Status Disponíveis

- 🟢 **Ativo**: Formulário disponível para preenchimento
- 🟡 **Padrão**: Formulário modelo padrão
- 🔴 **Inativo**: Formulário desabilitado temporariamente

### Informações Exibidas

Para cada formulário, você vê:
- **Nome do formulário** (ex: "FORM 9321 - Controle do Recebimento de Rancho")
- **Status atual** (Ativo, Padrão, Inativo)
- **Local de trabalho** (ex: "Belo Horizonte 2")
- **Data de criação/atualização**
- **Tipo de formulário** (Geral, Específico, etc.)

### Ações Disponíveis

Toque em qualquer formulário para acessar suas opções e detalhes.

---

## 5. Criando um Novo Formulário {#criando-novo-formulario}

### Passo 1: Iniciar Criação
1. Toque no botão **"+ Novo"** na tela principal
2. Selecione **"Novo Formulário"**

### Passo 2: Selecionar Modelo
1. Na tela "Selecione um Modelo", escolha entre os modelos disponíveis:
   - FORM 00 - Farol da Qualidade
   - FORM 9311 - Lista de Produtos Químicos para Limpeza
   - FORM 9315 - Controle da temperatura dos alimentos
   - FORM 9317 - Controle do resfriamento
   - FORM 9318 - Controle de Temperaturas das Câmaras
   - FORM 9326 - Controle de Sobra Limpa
   - E outros conforme disponibilidade da empresa

### Passo 3: Selecionar Local de Trabalho
1. Escolha o local onde o formulário será aplicado:
   - GERAL
   - Belo Horizonte 2
   - MG Extrema
   - Outros locais conforme sua empresa

### Passo 4: Configurar Formulário
1. **Nome do formulário**: Digite um nome descritivo
2. **Descrição**: Adicione uma descrição opcional
3. Toque em **"Criar Formulário"**

### Passo 5: Cancelar ou Confirmar
- **Cancelar**: Retorna à tela anterior sem salvar
- **Criar Formulário**: Confirma a criação e abre o formulário

---

## 6. Detalhes do Formulário {#detalhes-formulario}

Ao acessar um formulário, você visualiza:

### Cabeçalho
- **ID único** (ex: "06062025 - FORM 00 - Farol da Qualidade - Belo Horizonte 2")
- **Status** (Ativo/Inativo)
- **Tipo** (padrão, geral, etc.)
- **IDs de controle** (Local e Server)

### Indicadores de Sincronização
- 🟢 **Sincronizado**: Dados salvos no servidor
- 🟡 **Pendente**: Aguardando sincronização
- 🔴 **Falha**: Erro na sincronização
- 🟠 **Rascunho**: Salvo localmente

### Seções Principais

#### 📊 Registros
Lista todos os registros preenchidos neste formulário com:
- Status de sincronização
- Data de preenchimento
- Serviço verificado
- Local de verificação

---

## 7. Registros {#registros}

### Visualizando Registros
Na seção "Registros", você pode:
- **Pesquisar**: Use a barra de pesquisa para encontrar registros específicos
- **Filtrar**: Filtre por status, data ou outros critérios
- **Adicionar**: Toque no botão **"+"** para criar um novo registro

### Criando um Novo Registro

#### Passo 1: Escolher Ação
Ao tocar no botão **"+"**, selecione **"Concluir"** no modal de ações.

#### Passo 2: Preencher Campos Obrigatórios

Os campos marcados com ***** são obrigatórios:

1. **Data**: Selecione a data usando o seletor de calendário
2. **Serviço Verificado**: Escolha uma opção do dropdown (ex: "Bancadas")
3. **Local de Verificação**: Digite o local específico
4. **Descrição/Evidência**: Adicione detalhes sobre a verificação
5. **Classificação da Verificação**: Selecione o status (ex: "Em Desacordo com sequência construtiva")
6. **Qtd Unid. Verificadas**: Informe a quantidade

### Estados dos Registros

- **Pendente**: Registro salvo mas não sincronizado
- **Sincronizado**: Dados enviados com sucesso ao servidor
- **Erro**: Falha na sincronização
- **Rascunho**: Preenchimento em andamento

---

## 8. Estados e Status {#estados-status}

### Status de Sincronização

O aplicativo mostra claramente o status de cada item:

- **"ID Server: Não Sincronizado"**: Dados ainda não enviados ao servidor
- **"ID Server: [número]"**: Dados sincronizados com ID do servidor
- **"Pendente"**: Aguardando conexão para sincronizar
- **"Falha"**: Erro durante a sincronização

### Indicadores Visuais

- 🟢 Verde: Tudo funcionando normalmente
- 🟡 Amarelo: Atenção necessária
- 🔴 Vermelho: Erro ou problema
- 🟠 Laranja: Status intermediário

---

## 9. Sincronização {#sincronizacao}

### Como Funciona

O aplicativo sincroniza automaticamente quando há conexão com a internet. Todos os dados são salvos localmente primeiro, garantindo que nada seja perdido.

### Estados de Sincronização

1. **Offline**: Dados salvos apenas no dispositivo
2. **Sincronizando**: Enviando dados para o servidor
3. **Sincronizado**: Dados seguros no servidor
4. **Erro**: Falha na sincronização (dados mantidos localmente)

### Forçar Sincronização

- Puxe a tela para baixo para atualizar
- Verifique sua conexão com a internet
- Em caso de erro persistente, entre em contato com o suporte

---

## 10. Dicas e Boas Práticas {#dicas-boas-praticas}

### ✅ Boas Práticas

1. **Sempre preencha campos obrigatórios** (marcados com *)
2. **Use nomes descritivos** para formulários e registros
3. **Mantenha o app atualizado** para ter as últimas funcionalidades
4. **Verifique a sincronização** regularmente
5. **Faça backup dos dados importantes** antes de reinstalar o app

### ⚠️ Cuidados Importantes

- **Não desinstale o app** com dados não sincronizados
- **Mantenha espaço livre** no dispositivo para salvar dados temporários
- **Use conexão estável** para sincronização de dados grandes
- **Respeite as permissões** de acesso aos formulários da sua empresa

### 🔧 Resolução de Problemas

#### Problema: App não sincroniza
**Solução**: Verifique sua conexão com a internet e tente novamente

#### Problema: Formulário não carrega
**Solução**: Feche e abra o app novamente, ou reinstale se necessário

#### Problema: Dados perdidos
**Solução**: Dados são salvos localmente primeiro. Verifique na seção de rascunhos

---

## Suporte

Para dúvidas ou problemas técnicos, entre em contato com:
- **Email**: contato@nrxgestao.com.br
- **Telefone**: (31) 3333-4444
- **Site**: www.gnrx.com.br

---

*Manual atualizado para versão atual do aplicativo GNRx Formulários*