# Criar Colaborador

Esta página explica como adicionar um novo colaborador no Sistema GNRX Gestão de EPI.

## Visão Geral

O cadastro de colaboradores é fundamental para a gestão de EPIs, pois estabelece quem receberá os equipamentos de proteção e quais serão necessários com base nos riscos aos quais o trabalhador está exposto.

## Acessando a Tela de Criação

Para iniciar o cadastro de um novo colaborador:

1. No menu lateral, clique em **Estruturas**
2. Selecione **Colaboradores**
3. Na tela de listagem, clique no botão **Novo colaborador** no canto superior direito

![Botão Novo Colaborador](../../../assets/images/botao-novo-colaborador.png)

## Formulário de Cadastro

Ao clicar em "Novo colaborador", o sistema exibirá um modal com o formulário de criação:

![Formulário Novo Colaborador](../../../assets/images/formulario-novo-colaborador.png)

### Campos do Formulário

| Campo | Descrição | Obrigatoriedade | Exemplo |
|-------|-----------|-----------------|---------|
| **Nome** | Nome completo do colaborador | Obrigatório | "Victor Tavares" |
| **Email** | Endereço de e-mail para contato | Opcional | "victor.tavares@nrxgestao.com.br" |
| **CPF** | Número de CPF (apenas números) | Obrigatório | "12345678900" |
| **Telefone** | Número de telefone com DDD | Opcional | "+5531992088778" |
| **Matrícula** | Código de matrícula interna | Opcional | "123456" |
| **Início da Atividade** | Data de início das atividades | Opcional | "08/10/2024" |
| **Turno** | Período de trabalho | Opcional | "Manhã" |
| **PIN de Acesso** | Senha numérica de 6 dígitos para acesso ao app | Obrigatório | "123456" |

## Preenchendo o Formulário

1. Preencha os campos obrigatórios (Nome, CPF e PIN de Acesso)
2. Adicione informações complementares nos campos opcionais
3. Para o campo **PIN de Acesso**, defina uma senha de 6 dígitos numéricos que será utilizada pelo colaborador para:
   - Acessar o aplicativo móvel
   - Realizar confirmações de recebimento em tablets ou dispositivos móveis
4. Revise todas as informações inseridas
5. Clique no botão **Salvar** para criar o colaborador

## Após a Criação

Quando um novo colaborador é criado com sucesso:

1. O sistema exibe uma mensagem de confirmação
2. O colaborador é adicionado à lista
3. Você é redirecionado para a tela de detalhes do colaborador recém-criado

![Detalhes do Colaborador](../../../assets/images/detalhes-colaborador.png)

## Próximas Etapas Obrigatórias

Após o cadastro inicial, é necessário completar a configuração do colaborador com:

### 1. Vinculação a Unidades

É essencial associar o colaborador a pelo menos uma unidade física:

1. Na tela de detalhes do colaborador, localize a seção **Unidades**
2. Clique no botão **Adicionar Unidade**
3. Selecione a unidade desejada no modal exibido
4. Clique em **Associar**

> **Importante:** Um colaborador só poderá receber EPIs após estar vinculado a pelo menos uma unidade.

### 2. Vinculação a Setores

Após vincular a unidade, é necessário definir o setor:

1. Na seção de unidades, localize a unidade associada
2. Clique no botão **Setor** (ícone +)
3. Selecione o setor desejado no modal exibido
4. Clique em **Associar**

### 3. Vinculação a Cargos

Defina o cargo do colaborador:

1. Na estrutura hierárquica da unidade, ao lado do setor, clique no botão **Cargo**
2. Selecione o cargo correspondente no modal exibido
3. Clique em **Associar**

### 4. Vinculação a GHEs

**Esta é a etapa mais crítica, pois determinará quais EPIs o colaborador deverá receber:**

1. Na estrutura hierárquica da unidade, clique no botão **GHE**
2. Selecione o Grupo Homogêneo de Exposição adequado às atividades do colaborador
3. Clique em **Associar**

> **Fundamental:** A seleção correta do GHE é essencial, pois este vínculo determinará quais [riscos](../../configuracoes-iniciais/ghe/vincular-riscos.md) estão associados ao colaborador e, consequentemente, quais [EPIs](../../configuracoes-iniciais/ghe/vincular-epis.md) serão necessários.

## Considerações Importantes

- O CPF deve ser um número válido e único no sistema
- O PIN de acesso deve ter exatamente 6 dígitos numéricos
- Um colaborador não pode receber EPIs até que seja vinculado a um GHE
- A estrutura completa (Unidade > Setor > Cargo > GHE) é necessária para o funcionamento adequado do sistema

## Melhores Práticas

- **Dados Precisos**: Insira informações corretas e completas, especialmente CPF e nome
- **Vínculos Adequados**: Associe o colaborador aos GHEs que correspondem exatamente às suas atividades reais
- **Documentação**: Mantenha registros atualizados, especialmente após mudanças de função
- **PIN Seguro**: Informe ao colaborador seu PIN inicial e oriente-o a mantê-lo seguro
- **Cadastro Facial**: Após completar o cadastro básico, considere [cadastrar o reconhecimento facial](../reconhecimento-facial/cadastrar-face.md) para maior segurança nas entregas

## Erros Comuns e Soluções

| Erro | Solução |
|------|---------|
| "CPF já cadastrado" | Verifique se o colaborador já existe no sistema ou se o CPF foi digitado corretamente |
| "PIN deve conter 6 dígitos numéricos" | Certifique-se que o PIN tenha exatamente 6 números |
| "Erro ao salvar" | Verifique se todos os campos obrigatórios foram preenchidos corretamente |

---

*Última atualização: 16 de Maio de 2025*