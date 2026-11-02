---
description: Peça a compra de EPIs e produtos em 3 passos.
icon: cart-plus
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

# Criar uma solicitação de compra

**Para que serve:** pedir a compra de EPIs e produtos, para repor o estoque.

{% hint style="info" %}
**Quem pode fazer:** todas as roles, com a permissão de criar solicitações de compra.
{% endhint %}

## Antes de começar

* Os itens precisam estar cadastrados no inventário.

## Passo a passo

{% stepper %}
{% step %}
### Escolha o centro de estoque

Clique em **Inventário › Solicitações de Compra** e crie uma nova. Em **Selecione o Centro de Estoque (Opcional)**, escolha o centro ou **Global**.

<figure><img src="../.gitbook/assets/compras-nova-01.png" alt="Nova Solicitação - Compra com a escolha do centro de estoque"><figcaption><p>Nova Solicitação - Compra</p></figcaption></figure>
{% endstep %}

{% step %}
### Selecione os itens

Em **Selecione os Itens**, busque por nome, CA ou fabricante e informe a quantidade (e as variações, se houver).
{% endstep %}

{% step %}
### Revise e envie

Confira o **Resumo da Solicitação**. Se quiser, escreva as **Observações Adicionais** (ex.: urgente, prazo, preferência de fornecedor). Envie.
{% endstep %}
{% endstepper %}

## Deu errado?

| Mensagem na tela | O que fazer |
| --- | --- |
| "Selecione pelo menos um item" | Escolha os itens. |
| "Nenhum item disponível" | Cadastre itens no inventário para solicitar compras. |

## Dúvidas comuns

<details>

<summary>E depois de criar?</summary>

A solicitação é orçada e aprovada. Veja [Orçar e aprovar uma compra](orcar-e-aprovar-compra.md).

</details>

<details>

<summary>Posso cancelar?</summary>

Pode, com a permissão de cancelar solicitações de compra. Aparece "Solicitação cancelada com sucesso!".

</details>
