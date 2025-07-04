---
icon: boxes-stacked
---

# Editar Item

Esta página explica como editar as informações de um item existente no Sistema GNRX Gestão de EPI.

## Visão Geral

A edição de itens permite atualizar informações de EPIs já cadastrados no sistema, como correções de dados, atualização de certificados ou modificação de características e períodos de troca recomendados.

<figure><img src="../../.gitbook/assets/image (31).png" alt="" width="373"><figcaption><p>Editar Item Modal</p></figcaption></figure>

## Acessando a Função de Edição

Para editar um item existente:

1. No menu lateral, clique em **Inventário**
2. Selecione **Inventário de Items**
3. Localize o item que deseja editar na lista
4. Clique no ícone de lápis (editar) na coluna de opções

Alternativamente:

1. Acesse a tela de detalhes do item clicando no nome ou no ícone de visualização
2. Clique no botão **Atualizar o Item** no canto superior direito

## Informações Editáveis

Ao editar um item, você pode modificar:

### Itens com CA:

* **Nome**: Descrição principal do item
* **Data de Validade**: Atualização da validade do CA
* **Tempo de Troca**: Período recomendado para substituição
* **Fabricante**: Nome do fabricante ou fornecedor
* **Descrição**: Informações complementares sobre o item

### Itens sem CA:

* **Nome**: Descrição principal do item
* **Tempo de Troca**: Período opcional para substituição
* **Fabricante**: Nome do fabricante ou fornecedor
* **Descrição**: Informações complementares sobre o item

## Limitações de Edição

Alguns campos possuem restrições de edição:

* **Número do CA**: Não pode ser modificado após o cadastro inicial
* **Classificação NR-6**: Não pode ser alterada se houver estoque vinculado
* **Status Ativo/Inativo**: Alterado através da função específica de desativação

## Processo de Edição

1. Faça as alterações necessárias nos campos editáveis
2. Verifique cuidadosamente as informações atualizadas
3. Clique no botão **Salvar** para confirmar as modificações
4. O sistema validará as alterações e exibirá uma mensagem de confirmação

## Considerações Importantes

### Impacto em Outros Módulos

A edição de itens pode afetar:

* **Solicitações**: Alterações no nome podem impactar solicitações pendentes
* **Relatórios**: Modificações afetarão análises e históricos
* **Alertas**: Mudanças em datas de validade ou períodos de troca afetam notificações

### Registro de Alterações

O sistema mantém um histórico completo de edições:

* Todas as modificações são registradas com data, hora e usuário responsável
* É possível consultar o histórico de alterações para fins de auditoria
* As mudanças não afetam dados históricos de entregas já realizadas

## Melhores Práticas

Para uma gestão eficiente:

* Atualize prontamente informações obsoletas ou incorretas
* Mantenha os períodos de troca alinhados com recomendações do fabricante
* Documente na descrição o motivo de alterações significativas
* Revise regularmente a precisão das informações cadastradas

## Próximos Passos

Após editar um item, você pode:

* Verificar como o item aparece na [lista atualizada](listar-itens.md)
* [Adicionar variantes](../variantes/configurar-tipos-variante.md) se necessário
* Atualizar as [predefinições de período de troca](../lotes/gerenciar-validade.md)
* Conferir se as alterações refletem corretamente nos [relatórios](../relatorios/estoque-atual.md)

***

_Última atualização: 18 de Maio de 2025_
