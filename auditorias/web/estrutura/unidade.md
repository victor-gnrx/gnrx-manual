---
description: Como gerenciar unidades no sistema GNRX Auditorias
icon: building-2
---

# Unidades

O módulo de Unidades permite gerenciar os locais onde serão realizadas as auditorias, como filiais, fábricas, obras, embarcações, escritórios, etc. Cada unidade pode ter seus próprios setores e configurações específicas.

![Tela de unidades](/auditorias/assets/tela-unidades.png)

## Visão Geral da Tela de Unidades

A tela principal de Unidades exibe:

- **Total de unidades**: Número de unidades cadastradas no sistema
- **Lista de unidades**: Tabela com todas as unidades e suas informações principais, como nome, endereço, número de funcionários e situação

{% hint style="info" %}
A criação de novas unidades não está disponível diretamente na interface. Para adicionar uma nova unidade, é necessário entrar em contato com a equipe de suporte da GNRX para solicitar o cadastro.
{% endhint %}

## Atualizando uma Unidade

Para editar as informações de uma unidade existente:

1. Na lista de unidades, localize a unidade desejada
2. Clique no ícone de edição (lápis) na coluna "Opções"
3. No modal "Atualizar Unidade", você poderá modificar:
   - **Nome**: Nome da unidade
   - **Endereço**: Localização física completa
   - **CNPJ**: Documento de identificação da unidade
   - **Número de Funcionários**: Quantidade de colaboradores (usado para cálculos de multa)
   - **Descrição**: Informações adicionais sobre a unidade

![Formulário de atualização de unidade](/auditorias/assets/atualizar-unidade.png)

4. Após realizar as alterações necessárias, clique em **"Salvar"**

## Gerenciando Detalhes da Unidade

Ao clicar no nome de uma unidade na lista principal, você acessará a tela de detalhes, onde poderá gerenciar:

### Informações Básicas

A seção superior exibe:
- Nome da unidade
- Endereço completo
- Data de criação 
- Quantidade de funcionários

### Setores

A unidade pode ter múltiplos setores associados, que representam áreas específicas onde as auditorias serão realizadas.

#### Adicionando um Setor à Unidade

1. Na seção "Setores", clique no botão **"Adicionar setor"**
2. No modal "Associar Setor", selecione o setor desejado na lista suspensa
3. Clique em **"Associar"** para vincular o setor à unidade

![Modal de associação de setor](/auditorias/assets/associar-setor.png)

#### Removendo um Setor

Para remover um setor da unidade:
1. Localize o setor na lista
2. Clique no ícone de lixeira
3. Confirme a exclusão quando solicitado

### Emails para Relatórios

Esta seção permite configurar endereços de email que receberão automaticamente os relatórios de auditorias realizadas na unidade.

#### Adicionando um Email

1. Na seção "Emails para Relatórios", clique no botão **"Adicionar Email"**
2. Digite o endereço de email desejado
3. Clique em **"Adicionar"** para confirmar

![Configuração de emails para relatórios](/auditorias/assets/emails-relatorios.png)

#### Configurando um Email

Após adicionar um email, você pode configurar quais setores serão incluídos nos relatórios enviados:

1. Clique no ícone de engrenagem ao lado do email
2. No modal "Configurar Email", você terá duas opções:
   - **Receber de todos os setores**: O email receberá relatórios de auditorias de todos os setores da unidade
   - **Selecionar setores específicos**: Você poderá marcar quais setores serão incluídos

3. Para cada setor, você pode ativar a opção **"Solicitar Assinatura"**:
   - Quando ativada, o sistema enviará um link para que o destinatário assine eletronicamente a auditoria
   - Esta funcionalidade é útil para validações e aprovações remotas

![Configuração de setores para emails](/auditorias/assets/configurar-email-setores.png)

4. Clique em **"Salvar Configurações"** para aplicar as mudanças

#### Removendo um Email

Para remover um email da lista:
1. Clique no ícone de lixeira ao lado do email
2. Confirme a exclusão quando solicitado

### Usuários da Unidade

Esta seção mostra todos os usuários que têm acesso à unidade. A atribuição de usuários a unidades é gerenciada através do perfil de usuário.

## Pesquisando Unidades

Para localizar unidades específicas:

1. Use o campo de pesquisa no topo da lista
2. Digite parte do nome ou endereço da unidade
3. Clique no botão **"Pesquisar"** ou pressione Enter

## Visualizando Auditoria por Unidade

Para ver todas as auditorias realizadas em uma unidade específica:

1. Acesse a lista de Auditorias no menu principal
2. Use o filtro de Unidade para selecionar a unidade desejada
3. O sistema exibirá apenas as auditorias realizadas na unidade selecionada

## Importância do Número de Funcionários

O campo "Número de Funcionários" é utilizado para:

- Cálculos de dimensionamento de riscos
- Determinação de valores potenciais de multa
- Análises estatísticas de conformidade por tamanho de unidade

{% hint style="warning" %}
Mantenha o número de funcionários sempre atualizado, pois ele impacta diretamente os cálculos de multas potenciais em auditorias baseadas em NRs.
{% endhint %}

## Dicas de Gerenciamento de Unidades

- **Padronização de nomes**: Utilize um padrão consistente para nomear unidades
- **Emails estratégicos**: Configure emails para pessoas responsáveis por cada área
- **Revisão periódica**: Atualize regularmente as informações de endereço e número de funcionários
- **Setores adequados**: Associe todos os setores relevantes à unidade para facilitar a criação de auditorias

## Próximos Passos

Após configurar as unidades do sistema, você pode:

- [Configurar setores](setor.md)
- [Gerenciar usuários](usuario.md)