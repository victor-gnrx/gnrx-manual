---
icon: boxes-stacked
---

# Desativar Item

Esta página explica como desativar um item de EPI no Sistema GNRX Gestão de EPI.

## Visão Geral

A desativação de itens permite remover EPIs do catálogo ativo sem excluí-los permanentemente do sistema, preservando o histórico de uso e mantendo a integridade dos registros. Itens desativados não podem ser incluídos em novas solicitações, mas continuam visíveis para consulta e relatórios.

## Quando Desativar um Item

É recomendado desativar itens nas seguintes situações:

* Quando o CA for definitivamente cancelado ou não renovado
* Ao descontinuar o uso de determinado modelo de EPI
* Para substituir por versões mais atualizadas do mesmo equipamento
* Quando houver erro de cadastro e não for possível corrigir por edição
* Para EPIs que não serão mais adquiridos pela empresa

## Acessando a Função de Desativação

Para desativar um item:

1. No menu lateral, clique em **Inventário**
2. Selecione **Inventário de Items**
3. Localize o item que deseja desativar na lista
4. Clique no ícone de lixeira (excluir) na coluna de opções

## Processo de Desativação

Ao clicar no ícone de exclusão:

1. O sistema exibirá um diálogo de confirmação
2. O diálogo informará as implicações da desativação
3. Você deverá confirmar a ação clicando em **Desativar**
4. O sistema processará a solicitação e mudará o status do item para "Inativo"

## Verificações de Segurança

O sistema realiza verificações automáticas antes de permitir a desativação:

* **Itens com estoque em uso**: Não podem ser desativados até que todos os equipamentos sejam devolvidos
* **Itens com solicitações pendentes**: Exigem tratamento das solicitações antes da desativação
* **Itens com histórico extenso**: Receberão alertas adicionais sobre o impacto da desativação

## Efeitos da Desativação

Após desativar um item:

* O status na lista de itens mudará para "Inativo"
* O item não aparecerá mais nas opções de novas solicitações
* Permanecerá visível nas consultas e relatórios históricos
* Manterá seu estoque e dados para fins de rastreabilidade
* Poderá ser reativado se necessário

## Reativando um Item

Para reverter a desativação:

1. Acesse a lista de itens
2. Utilize o filtro para mostrar itens inativos (se não estiverem visíveis por padrão)
3. Clique no item inativo para abrir seus detalhes
4. Utilize a opção de reativação disponível na tela de detalhes

## Melhores Práticas

Para um gerenciamento eficiente:

* Avalie cuidadosamente a necessidade de desativação
* Notifique as equipes relevantes antes de desativar itens em uso
* Documente o motivo da desativação para referência futura
* Estabeleça um processo regular de revisão para itens obsoletos
* Prefira a desativação à exclusão permanente para manter a integridade dos dados

## Considerações Importantes

### Impacto em Outros Módulos

A desativação afeta:

* **Solicitações**: Itens desativados não estarão disponíveis para novas solicitações
* **Relatórios**: Continuarão aparecendo em análises históricas
* **Ficha EPI Digital**: Permanecerão nos registros de entregas passadas

### Alternativa à Desativação

Em alguns casos, em vez de desativar completamente:

* Considere atualizar a data de validade do CA
* Defina estoque zero para impedir novas solicitações
* Atualize a descrição indicando a situação do item

## Próximos Passos

Após desativar um item, recomenda-se:

* Verificar a [lista de itens](listar-itens.md) para confirmar a mudança de status
* Consultar [relatórios de estoque](../relatorios/estoque-atual.md) para verificar o impacto
* Avaliar a necessidade de [cadastrar itens substitutos](criar-item-com-ca.md)
* Revisar as [predefinições de período](../lotes/gerenciar-validade.md) que incluíam o item desativado

***

_Última atualização: 18 de Maio de 2025_
