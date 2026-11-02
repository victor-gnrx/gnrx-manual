---
description: Adicione os orçamentos de cada item e aprove a compra.
icon: file-invoice-dollar
layout:
  width: default
  title:
    visible: true
  description:
    visible: true
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
  metadata:
    visible: false
  tags:
    visible: true
  actions:
    visible: true
---

# Orçar e aprovar uma compra

**Para que serve:** cotar cada item com os fornecedores, escolher o orçamento e aprovar ou rejeitar a compra.

{% hint style="info" %}
**Quem pode fazer:** Supervisor, Gestor ou Administrador, com a permissão de adicionar e aprovar orçamentos e a de aprovar solicitações de compra.
{% endhint %}

## Antes de começar

* Para usar o preço do catálogo, [vincule os itens aos fornecedores](../gestao-estoque/fornecedores/vincular-itens.md).

## Passo a passo

{% stepper %}
{% step %}
### Adicione os orçamentos

Abra a solicitação. Em cada item, use **Adicionar orçamento**. Escolha uma **Sugestão do catálogo** (**Melhor preço** ou **Melhor qualidade**) ou o fornecedor à mão, e informe o **Preço unitário**, o **Prazo de entrega (dias)** e a **Observação** (ex.: frete incluso). Clique em **Adicionar**. Aparece "Orçamento adicionado.".

<figure><img src="../.gitbook/assets/compras-orcamento-01.png" alt="Janela Adicionar orçamento com as sugestões do catálogo e os campos de preço e prazo"><figcaption><p>Adicionar orçamento</p></figcaption></figure>
{% endstep %}

{% step %}
### Aprove o orçamento

Escolha o orçamento de cada item e aprove. Aparece "Orçamento aprovado.".
{% endstep %}

{% step %}
### Aprove a solicitação

Aprove ou rejeite a solicitação. Aparece "Solicitação aprovada com sucesso!" ou "Solicitação rejeitada com sucesso!". Se a empresa usa [fluxo de aprovação](../fluxos-aprovacao/decidir-aprovacao.md), a decisão é pelo fluxo.
{% endstep %}
{% endstepper %}

## Deu errado?

{% hint style="warning" %}
**"Este fornecedor já tem um orçamento para este item."**: edite o orçamento que já existe.
{% endhint %}

## Dúvidas comuns

<details>

<summary>De onde vem o preço sugerido?</summary>

Do vínculo cadastrado do fornecedor com o item. Se você digitar o preço, ele fica marcado como manual.

</details>

<details>

<summary>Posso anexar a cotação?</summary>

Pode. Na solicitação, anexe o arquivo. Aparece "O arquivo foi anexado à solicitação.".

</details>
