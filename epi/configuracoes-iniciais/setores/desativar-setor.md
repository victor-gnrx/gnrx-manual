# Desativar Setor

Esta página explica como desativar um setor existente no Sistema GNRX Gestão de EPI, bem como as implicações desta ação.

## Visão Geral

A desativação de setores é utilizada quando uma área funcional deixa de existir na estrutura organizacional, mas você precisa manter seu histórico no sistema. Diferente da exclusão definitiva, a desativação preserva todos os registros associados para fins de auditoria e consulta.

## Quando Desativar um Setor

As situações mais comuns para desativação incluem:

* Reorganização estrutural da empresa
* Fusão de departamentos
* Descontinuação de uma linha de atividade
* Substituição por nova estrutura departamental
* Correção de duplicidade (múltiplos setores para a mesma função)

## Acessando a Função de Desativação

Para desativar um setor:

1. No menu lateral, clique em **Estruturas**
2. Selecione **Setores**
3. Na lista de setores, localize o setor desejado
4. Clique no ícone de **Excluir/Desativar** (símbolo de lixeira) na coluna de ações

![Desativar Setor](<../../.gitbook/assets/image (13) (1).png>)

## Processo de Desativação

Ao iniciar a desativação, o sistema apresentará um diálogo de confirmação:

![Diálogo de Confirmação](<../../.gitbook/assets/image (16) (1).png>)

O diálogo inclui:

1. Alerta sobre as consequências da desativação
2. Informações sobre itens associados (colaboradores)
3. Botões de "Cancelar" e "Inativar"

Para prosseguir:

1. Clique em **Inativar**
2. O sistema processará a solicitação e exibirá uma mensagem de confirmação

## Impacto da Desativação

Quando um setor é desativado:

### O que acontece:

* O setor recebe o status "Inativo" na lista de setores
* Ele deixa de aparecer em listas de seleção para novas associações
* Relatórios padrão filtram o setor, a menos que explicitamente incluído
* O histórico completo permanece acessível para consulta

### O que NÃO acontece:

* O registro do setor não é excluído do banco de dados
* Históricos de entregas de EPIs associados ao setor não são removidos
* Vínculos existentes com colaboradores são mantidos, mas marcados como inativos
* Documentos e registros legais permanecem intactos

## Verificações Prévias à Desativação

Antes de desativar um setor, o sistema verifica:

| Item                       | Verificação                                   | Ação Recomendada                  |
| -------------------------- | --------------------------------------------- | --------------------------------- |
| **Colaboradores Ativos**   | Se há funcionários ativos vinculados ao setor | Transferir para outros setores    |
| **Solicitações Pendentes** | Se existem solicitações de EPIs em aberto     | Concluir ou cancelar solicitações |

## Reativando um Setor

Para reativar um setor previamente desativado, entre em contato com o suporte.

## Considerações Importantes

* A desativação deve ser utilizada em vez da exclusão quando o setor já possui histórico
* Considere a reatribuição de colaboradores antes da desativação
* Informe os usuários do sistema sobre mudanças na estrutura organizacional
* Documente adequadamente o motivo da desativação para referência futura
* Verifique o impacto em relatórios históricos antes de proceder

## Alternativas à Desativação

Em alguns casos, existem alternativas preferíveis à desativação:

* **Renomeação**: Se apenas o nome mudou, edite o setor em vez de desativá-lo
* **Reorganização**: Se houve fusão de departamentos, considere manter um dos setores e transferir os colaboradores
* **Atualização de Descrição**: Se a função mudou mas a estrutura permanece, atualize a descrição

## Impacto nas Unidades Vinculadas

A desativação de um setor afeta sua relação com as unidades:

* O setor desativado não aparecerá mais nas listas de setores das unidades
* Os vínculos históricos são preservados para fins de rastreabilidade
* Novos colaboradores não poderão ser atribuídos ao setor desativado

## Próximos Passos após Desativação

Após desativar um setor, considere:

1. Verificar os colaboradores que estavam associados ao setor
2. Atualizar documentação interna sobre a estrutura organizacional
3. Comunicar a mudança às equipes relevantes

***

_Última atualização: 16 de Maio de 2025_
