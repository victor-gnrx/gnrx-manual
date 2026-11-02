---
description: Dar entrada de um item com variantes.
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

# Dar entrada de um item com variantes

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

Se o item tem variantes (ex.: tamanho), depois das **Informações Básicas** aparece **Distribuição por Variantes**. Use **Adicionar Combinação** para dizer quanto entra de cada combinação (ex.: 10 do M, 5 do G). O **Status da Distribuição** mostra se a soma bate com a **Quantidade Total**. Depois, distribua por centro de estoque e clique em **Confirmar Entrada**.
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
