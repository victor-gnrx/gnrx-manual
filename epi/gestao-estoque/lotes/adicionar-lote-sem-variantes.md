---
description: Dar entrada de um item sem variantes.
icon: circle-plus
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

# Dar entrada de um item sem variantes

**Para que serve:** registrar a chegada do item e dizer onde ele fica guardado.

{% hint style="info" %}
**Quem pode fazer:** Administrador, com a permissão de gerenciar o estoque de EPIs.
{% endhint %}

## Antes de começar

* Veja o passo a passo completo em [Dar entrada no estoque](../itens/adicionar-lote.md).

## Passo a passo

{% stepper %}
{% step %}
### Abra a entrada

Abra o item e clique em **Adicionar Estoque**. Preencha as **Informações Básicas** e clique em **Próximo Passo**.
{% endstep %}

{% step %}
### Distribua

Se o item não tem variantes, depois das **Informações Básicas** você distribui a **Quantidade Total** entre os centros de estoque: **Dividir igualmente entre todos**, **Enviar tudo para esta unidade** ou uma quantidade por centro. Quando aparecer **Distribuição completa**, clique em **Confirmar Entrada**.
{% endstep %}
{% endstepper %}

## Deu errado?

{% hint style="warning" %}
**"Você precisa distribuir os itens em pelo menos uma unidade"**: distribua a quantidade.
{% endhint %}

## Dúvidas comuns

<details>

<summary>Errei a distribuição.</summary>

Use **Limpar distribuição** (ou **Limpar tudo**) e distribua de novo.

</details>

<details>

<summary>Qual a diferença para o lote do fabricante?</summary>

O número do lote é o que você informa na entrada (ex.: CA0001-L57).

</details>
