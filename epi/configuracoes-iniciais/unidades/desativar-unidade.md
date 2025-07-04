# Desativar Unidade

Esta página explica como desativar uma unidade existente no Sistema GNRX Gestão de EPI, bem como as implicações desta ação.

## Visão Geral

A desativação de unidades é utilizada quando uma localidade física não está mais operacional, mas você deseja manter seu histórico no sistema. Ao contrário da exclusão definitiva, a desativação preserva todos os registros associados para fins de auditoria e consulta.

## Quando Desativar uma Unidade

As situações mais comuns para desativação incluem:

* Fechamento definitivo da localidade
* Fusão de duas ou mais unidades
* Reorganização estrutural da empresa
* Suspensão temporária das operações
* Substituição por nova unidade

## Acessando a Função de Desativação

1. No menu lateral, clique em **Estruturas**
2. Selecione **Unidades**
3. Na lista de unidades, localize a unidade desejada
4. Clique no ícone de **Excluir/Desativar** (símbolo de lixeira) na coluna de ações

<figure><img src="../../.gitbook/assets/image (13) (1).png" alt=""><figcaption><p>Desativar via lista</p></figcaption></figure>

## Processo de Desativação

Ao iniciar a desativação, o sistema apresentará um diálogo de confirmação:

<figure><img src="../../.gitbook/assets/image (14) (1).png" alt=""><figcaption></figcaption></figure>

Para prosseguir:

1. Clique em Inativar
2. O sistema processará a solicitação e exibirá uma mensagem de confirmação

## Impacto da Desativação

Quando uma unidade é desativada:

### O que acontece:

* A unidade recebe o status "Inativo" na lista de unidades
* Ela deixa de aparecer em listas de seleção para novas associações
* Relatórios padrão filtram a unidade, a menos que explicitamente incluída
* <mark style="background-color:green;">**O histórico completo permanece acessível para consulta**</mark>

### O que NÃO acontece:

* O registro da unidade não é excluído do banco de dados
* Históricos de entregas de EPIs não são removidos
* Vínculos existentes com colaboradores e setores são mantidos, mas marcados como inativos
* Documentos e registros legais permanecem intactos

## Verificações Prévias à Desativação

Antes de desativar uma unidade, o sistema verifica:

| Item                       | Verificação                                    | Ação Recomendada                             |
| -------------------------- | ---------------------------------------------- | -------------------------------------------- |
| **Colaboradores Ativos**   | Se há funcionários ativos vinculados à unidade | Transferir para outras unidades ou desativar |
| **Solicitações Pendentes** | Se existem solicitações de EPIs em aberto      | Concluir ou cancelar solicitações            |
| **Estoque Disponível**     | Se há EPIs em estoque nesta unidade            | Transferir para outras unidades              |
| **GHEs Exclusivos**        | Se existem GHEs exclusivos desta unidade       | Revisar e realocar se necessário             |

## Reativando uma Unidade

Para reativar uma unidade previamente desativada entre em contato com o suporte.

## Considerações Importantes

* A desativação é diferente da exclusão definitiva, que não é permitida para unidades com histórico
* Relatórios históricos continuam mostrando a unidade para períodos em que estava ativa
* Para fins de conformidade legal, o histórico de EPIs de unidades desativadas permanece acessível
* Coordene com o departamento de TI antes de desativar unidades com grande volume de registros

## Alternativas à Desativação

Em alguns casos, existem alternativas preferíveis à desativação:

* **Renomeação**: Se apenas o nome mudou, edite a unidade em vez de desativá-la
* **Relocalização**: Se a unidade mudou de endereço, atualize os dados cadastrais
* **Reorganização**: Se houve fusão, considere manter uma das unidades e transferir os registros (Verificar com o departamento de TI para fazer a transferência)

***

_Última atualização: 16 de Maio de 2025_
