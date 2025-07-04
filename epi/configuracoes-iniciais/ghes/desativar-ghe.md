---
icon: cubes
---

# Desativar GHE

Esta página explica como desativar um Grupo Homogêneo de Exposição (GHE) existente no Sistema GNRX Gestão de EPI, bem como as implicações desta ação.

## Visão Geral

A desativação de GHEs é utilizada quando um grupo específico deixa de existir na organização ou quando há uma reformulação significativa da estrutura de exposição a riscos. Diferente da exclusão definitiva, a desativação preserva o histórico para fins de auditoria e rastreabilidade.

## Quando Desativar um GHE

As situações mais comuns para desativação incluem:

* Extinção de uma função ou atividade específica
* Reorganização de processos que alterou o perfil de exposição
* Mudanças tecnológicas que eliminaram determinados riscos
* Consolidação ou divisão de grupos existentes
* Correção de GHEs criados erroneamente

## Acessando a Função de Desativação

Para desativar um GHE:

1. No menu lateral, clique em **Estruturas**
2. Selecione **GHEs**
3. Na lista de GHEs, localize o grupo desejado
4. Clique no ícone de **Excluir/Desativar** (símbolo de lixeira) na coluna de ações

![Desativar GHE](<../../.gitbook/assets/image (13) (1).png>)

## Processo de Desativação

Ao iniciar a desativação, o sistema apresentará um diálogo de confirmação:

<figure><img src="../../.gitbook/assets/image (29) (1).png" alt=""><figcaption></figcaption></figure>

Para prosseguir:

1. Clique em Inativar
2. O sistema processará a solicitação e exibirá uma mensagem de confirmação

## Impacto da Desativação

Quando um GHE é desativado:

### O que acontece:

* O GHE recebe o status "Inativo" na lista de grupos
* Ele deixa de aparecer em listas de seleção para novas associações
* Relatórios padrão filtram o GHE, a menos que explicitamente incluído
* O histórico completo permanece acessível para consulta

### O que NÃO acontece:

* O registro do GHE não é excluído do banco de dados
* Históricos de entregas de EPIs associados ao grupo não são removidos
* Vínculos existentes com colaboradores são mantidos, mas marcados como inativos
* Documentos e registros legais permanecem intactos

## Verificações Prévias à Desativação

Antes de desativar um GHE, o sistema verifica:

| Item                       | Verificação                                 | Ação Recomendada                      |
| -------------------------- | ------------------------------------------- | ------------------------------------- |
| **Colaboradores Ativos**   | Se há funcionários ativos vinculados ao GHE | Transferir para outros GHEs adequados |
| **Solicitações Pendentes** | Se existem solicitações de EPIs em aberto   | Concluir ou cancelar solicitações     |

## Reativando um GHE

Para reativar um GHE previamente desativado entre em contato com o suporte.

## Considerações Importantes

* A desativação de um GHE deve ser precedida pela reatribuição dos colaboradores a outros grupos apropriados
* Considere o impacto nos relatórios históricos e documentação legal
* A desativação não elimina a responsabilidade por EPIs já entregues
* Consulte o setor de SST antes de desativar GHEs com histórico significativo

## Alternativas à Desativação

Em alguns casos, existem alternativas preferíveis à desativação:

* **Atualização**: Se apenas os riscos mudaram, mantenha o GHE e atualize seus riscos e EPIs
* **Renomeação**: Se apenas o nome precisa mudar, edite o GHE em vez de desativá-lo
* **Consolidação**: Se dois GHEs similares existem, considere unificar em vez de desativar

## Impacto na Documentação Legal

A desativação de GHEs pode ter implicações para documentação oficial de SST:

* Certifique-se de que as mudanças estão refletidas no PGR/PPRA
* Documente a transição em relatórios internos

## Impacto nos Colaboradores

Quando um GHE é desativado, os colaboradores anteriormente vinculados:

* Devem ser associados a novos GHEs apropriados
* Continuam tendo acesso ao histórico de EPIs recebidos
* Podem precisar de novos EPIs se os riscos mudaram
* Devem ser informados sobre mudanças nos requisitos de proteção

## Logs e Auditoria

O sistema mantém registros detalhados das desativações:

* Data e hora da desativação
* Usuário que executou a ação
* Motivo informado
* Estado dos vínculos no momento da desativação

Estes logs estão disponíveis para administradores do sistema na seção de Auditoria.

## Melhores Práticas

* Desative GHEs apenas quando houver justificativa técnica sólida
* Documente claramente as razões para a desativação
* Coordene a desativação com atualizações nos documentos oficiais de SST
* Informe as equipes de segurança sobre as mudanças realizadas
* Verifique a conformidade dos colaboradores após a transição para novos GHEs

***

_Última atualização: 16 de Maio de 2025_
