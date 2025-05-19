# Criar Item com CA

Esta página explica como cadastrar um novo item de EPI com Certificado de Aprovação (CA) no Sistema GNRX Gestão de EPI.

## Visão Geral

O cadastro de itens com CA é fundamental para a gestão adequada de Equipamentos de Proteção Individual que possuem certificação obrigatória conforme a NR-6. Este processo permite registrar todas as informações essenciais, incluindo número do certificado, fabricante, validade e período de troca recomendado.

![Criar Item com CA](../../../assets/images/criar-item-ca.png)

## Acessando o Formulário

Para criar um novo item com CA:

1. No menu lateral, clique em **Inventário**
2. Selecione **Inventário de Items**
3. Clique no botão **Novo Item** no canto superior direito da tela

## Preenchendo o Formulário

O modal "Criar Item" será exibido com os seguintes campos:

### 1. Informações Básicas

- **Nome**: Digite o nome completo do EPI (ex: "Protetor Auditivo tipo concha L-320 C")
- **Número CA**: Ative o toggle (botão de alternância) e digite o número do Certificado de Aprovação emitido pelo Ministério do Trabalho
- **Data de Validade**: Selecione a data de validade do CA no formato DD/MM/AAAA

### 2. Classificação do EPI

- **EPI (NR-6)**: Selecione o tipo de EPI conforme a classificação da NR-6 no menu suspenso
  - Esta seleção é obrigatória e determina a categoria oficial do equipamento
  - Os EPIs são organizados conforme a parte do corpo que protegem (cabeça, membros superiores, etc.)

### 3. Período de Troca

- **Tempo de Troca (Dias)**: Ative o toggle e digite o período recomendado para substituição periódica do EPI em dias
  - Exemplo: "180" para EPIs que devem ser substituídos a cada 6 meses
  - Este valor será usado como referência para o sistema alertar sobre necessidades de substituição

### 4. Informações do Fabricante e Complementares

- **Fabricante**: Digite o nome do fabricante do EPI (ex: "LIBUS DO BRASIL EQUIPAMENTOS LTDA")
- **Descrição (Opcional)**: Campo para adicionar informações complementares como características, aplicações recomendadas ou observações importantes

## Salvando o Cadastro

Após preencher todos os campos necessários:

1. Verifique se as informações estão corretas, especialmente o número do CA e a data de validade
2. Clique no botão **Salvar** no canto inferior direito do modal
3. O sistema irá processar o cadastro e, se bem-sucedido, exibirá uma mensagem de confirmação
4. O novo item será adicionado à lista de itens disponíveis

## Considerações Importantes

### Sobre o Número do CA

- O Certificado de Aprovação (CA) é emitido pelo Ministério do Trabalho e Emprego
- Deve ser único e válido conforme registros oficiais
- Pode ser verificado no site do Ministério do Trabalho
- É obrigatório para todos os EPIs conforme a NR-6

### Sobre a Data de Validade

- Refere-se à validade do CA, não necessariamente à validade física do produto
- Os lotes específicos podem ter datas de validade diferentes que serão gerenciadas separadamente
- O sistema alertará sobre CAs próximos do vencimento

### Sobre o Tempo de Troca

- É utilizado como referência para substituição periódica
- Pode ser definido conforme recomendação do fabricante ou normas internas
- Não está necessariamente relacionado à validade do CA
- Impacta diretamente no planejamento de estoque e orçamento

## Próximos Passos

Após cadastrar um item com sucesso, você pode:

1. [Adicionar variantes](../variantes/configurar-tipos-variante.md) como tamanho, cor, etc.
2. [Cadastrar um lote](../lotes/adicionar-lote.md) para registrar entrada no estoque
3. Configurar [períodos de troca personalizados](../lotes/gerenciar-validade.md) por unidade
4. Verificar o [item na listagem](./listar-itens.md) para confirmar o cadastro

## Verificação da Conformidade

Para garantir a conformidade legal, é essencial verificar as seguintes informações:

- O CA deve ser válido e estar dentro do prazo de validade
- As informações do fabricante devem corresponder às do certificado oficial
- O tipo de EPI selecionado deve estar de acordo com a classificação do CA

## Edição Posterior

Caso seja necessário corrigir informações após o cadastro:

1. Localize o item na [lista de itens](./listar-itens.md)
2. Clique no ícone de edição (lápis) na coluna de opções
3. Faça as alterações necessárias
4. Salve as modificações

> **Importante**: Algumas mudanças, como o número do CA, podem afetar a rastreabilidade e conformidade. Realize-as com cautela.

---

*Última atualização: 18 de Maio de 2025*