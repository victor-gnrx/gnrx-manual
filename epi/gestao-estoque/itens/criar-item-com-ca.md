# Cadastro de Item com CA

Esta página explica como cadastrar um novo item de EPI com Certificado de Aprovação (CA) no Sistema de Gestão de EPI GNRX.

## O que é um CA?

O Certificado de Aprovação (CA) é um documento emitido pelo Ministério do Trabalho que atesta que um Equipamento de Proteção Individual (EPI) está em conformidade com as normas técnicas de segurança. Itens com CA são obrigatórios para a maioria das funções com riscos ocupacionais.

## Acessando a Tela de Cadastro

1. No menu lateral, acesse **Gestão de Estoque**
2. Selecione **Itens**
3. Clique no botão **Novo Item** no canto superior direito
4. Na tela de seleção, escolha a opção **Com CA**

![Novo Item com CA](../../../assets/images/novo-item-ca.png)

## Formulário de Cadastro

O cadastro de um item com CA é dividido em seções:

### Informações Básicas

![Formulário Informações Básicas](../../../assets/images/form-item-info-basicas.png)

| Campo | Descrição | Obrigatório |
|-------|-----------|-------------|
| Nome | Nome descritivo do item | Sim |
| Número CA | Número do Certificado de Aprovação | Sim |
| Tipo de EPI | Tipo de EPI conforme catálogo NR-6 | Sim |
| Fabricante | Nome do fabricante do equipamento | Sim |
| Descrição | Detalhes adicionais sobre o item | Não |

> **Dica:** O sistema possui uma base de dados integrada com os CAs registrados no sistema CAEPI do Ministério do Trabalho. Ao digitar o número do CA, o sistema pode preencher automaticamente alguns campos. Verifique sempre se as informações estão corretas.

### Informações de Estoque e Validade

![Estoque e Validade](../../../assets/images/form-item-estoque-validade.png)

| Campo | Descrição | Obrigatório |
|-------|-----------|-------------|
| Custo Unitário | Valor médio unitário em R$ | Sim |
| Controle de Estoque | Ativar controle de quantidades | Sim |
| Estoque Inicial | Quantidade inicial disponível | Não |
| Estoque Mínimo | Nível para alerta de estoque baixo | Não |
| Controle de Validade | Ativar gestão de datas de validade | Sim |
| Tempo para Troca | Periodicidade padrão para substituição em dias | Não |

### Configuração de Variantes (Opcional)

![Configuração de Variantes](../../../assets/images/form-item-variantes.png)

Nesta seção, você pode configurar se o item possui variantes como tamanho, cor, etc.

1. Marque a opção **Este item possui variantes**
2. Clique em **Adicionar Tipo de Variante**
3. Digite o nome da variante (ex: "Tamanho")
4. Defina se é obrigatório informar esta variante
5. Repita o processo para adicionar mais tipos de variantes, se necessário

> **Nota:** A configuração detalhada das variantes será feita após salvar o item inicial. Para mais informações, consulte a seção [Configurar Tipos de Variante](../variantes/configurar-tipos-variante.md).

## Finalizando o Cadastro

1. Revise todas as informações preenchidas
2. Clique no botão **Salvar**
3. O sistema exibirá uma mensagem de confirmação
4. Se configurou variantes, o sistema redirecionará para a tela de configuração detalhada de variantes

## Próximos Passos Recomendados

Após cadastrar um novo item com CA, recomendamos:

1. [Configurar as variantes](../variantes/configurar-tipos-variante.md) detalhadamente, se aplicável
2. [Adicionar um lote](../lotes/adicionar-lote.md) para registrar a entrada efetiva no estoque
3. [Vincular o item aos GHEs](../../configuracoes-iniciais/ghe/vincular-epis.md) apropriados

## Erros Comuns

| Erro | Solução |
|------|---------|
| "CA não encontrado na base do Ministério" | Verifique se o número está correto ou cadastre manualmente as informações |
| "CA já cadastrado no sistema" | Verifique se o item já existe ou se há erro na digitação do CA |
| "Tipo de EPI inválido" | Selecione um tipo válido do catálogo NR-6 ou cadastre um tipo personalizado |

## Observações Importantes

- Items com CA devem ter todas as informações exatamente como consta no certificado
- Mantenha os dados de validade do CA atualizados, pois expiração do CA pode gerar não conformidades
- Recomenda-se anexar uma cópia do certificado ou link para o documento no sistema CAEPI