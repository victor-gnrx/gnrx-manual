# Vincular Unidades

Esta página explica como associar colaboradores a unidades no Sistema GNRX Gestão de EPI.

## Visão Geral

A vinculação de colaboradores a unidades é um passo fundamental no sistema, pois determina onde o funcionário está fisicamente alocado. Esta associação é pré-requisito para a definição de setores, cargos e GHEs, que por sua vez determinam quais EPIs serão necessários.

## Importância da Vinculação a Unidades

A correta associação entre colaboradores e unidades é essencial para:

* Organizar adequadamente a estrutura hierárquica no sistema
* Possibilitar a posterior vinculação a setores específicos
* Definir de qual estoque os EPIs serão retirados
* Gerar relatórios precisos por localidade
* Facilitar a gestão descentralizada de equipamentos

## Acessando a Tela de Vinculação

Para vincular um colaborador a uma unidade:

1. No menu sperior, clique em **Estruturas**
2. Selecione **Colaboradores**
3. Localize e clique no colaborador desejado para abrir seus detalhes (Olho)
4. Na tela de detalhes, localize a seção **Unidades**
5. Clique no botão **Adicionar Unidade**

<figure><img src="../../.gitbook/assets/image (9).png" alt=""><figcaption><p>Seção de unidades</p></figcaption></figure>

## Processo de Vinculação

Ao clicar em "Adicionar Unidade", o sistema exibirá um modal para seleção:

![Modal Associar Unidade](<../../.gitbook/assets/image (10).png>)

1. No campo de seleção, clique para abrir a lista de unidades disponíveis
2. Selecione a unidade desejada
3. Clique no botão **Associar**
4. O sistema processará a vinculação e exibirá a unidade na estrutura hierárquica do colaborador

## Estrutura Hierárquica

Após a vinculação, a unidade aparecerá na estrutura hierárquica do colaborador:

<figure><img src="../../.gitbook/assets/image (11).png" alt=""><figcaption><p>Estrutura Hierarquica</p></figcaption></figure>

Esta visualização mostra:

* A unidade vinculada
* Setores associados (se houver)
* Cargos definidos (se houver)
* GHEs vinculados (se houver)

## Vinculação a Múltiplas Unidades

Um colaborador pode estar vinculado a mais de uma unidade, caso atue em diferentes localidades:

1. Para cada unidade adicional, repita o processo de vinculação
2. Cada unidade aparecerá como um item separado na estrutura hierárquica
3. O colaborador poderá receber EPIs específicos para cada unidade onde atua

## Removendo Vínculos

Para remover a associação entre um colaborador e uma unidade:

1. Na estrutura hierárquica, localize a unidade que deseja desvincular
2. Clique no ícone de remoção (lixeira) ao lado da unidade
3. Confirme a ação no diálogo exibido
4. A unidade e todos seus vínculos relacionados (setores, cargos e GHEs) serão removidos

> **Importante:** A remoção de uma unidade também excluirá todos os vínculos hierárquicos abaixo dela (setores, cargos e GHEs). Esta ação não afeta o histórico de EPIs já entregues.

## Próximos Passos após Vinculação

Após vincular um colaborador a uma unidade, é necessário continuar a configuração:

1. [Vincular a Setores](vincular-setores.md) - Definir em qual área o colaborador atua
2. Associar a um Cargo - Definir sua função específica
3. [Vincular a GHEs](vincular-ghe.md) - **Etapa crucial** que determinará quais EPIs serão necessários

> **Fundamental:** A estrutura completa (Unidade > GHE) é necessária para que o sistema possa determinar corretamente quais EPIs devem ser fornecidos ao colaborador.

## Considerações Importantes

* Um colaborador deve estar vinculado a pelo menos uma unidade para receber EPIs
* A vinculação a uma unidade afeta de qual estoque os EPIs serão retirados
* Colaboradores que atuam em múltiplas unidades devem ter todas elas registradas
* Alterações nos vínculos não afetam entregas já realizadas
* A estrutura hierárquica deve refletir a realidade operacional da empresa

## Melhores Práticas

* Mantenha as vinculações atualizadas quando houver transferências entre unidades
* Certifique-se de que a unidade selecionada corresponde à localização física real do colaborador
* Para colaboradores que atuam em múltiplas unidades, defina a principal primeiro
* Revise periodicamente os vínculos para garantir que refletem a situação atual
* Ao desativar uma unidade, lembre-se de transferir os colaboradores para outras unidades ativas

## Erros Comuns e Soluções

| Erro                     | Solução                                                                |
| ------------------------ | ---------------------------------------------------------------------- |
| "Unidade não encontrada" | Verifique se a unidade foi previamente cadastrada no sistema           |
| "Erro ao vincular"       | Certifique-se de que tanto o colaborador quanto a unidade estão ativos |
| "Não é possível remover" | Verifique se há entregas de EPIs pendentes relacionadas à unidade      |

***

_Última atualização: 16 de Maio de 2025_
