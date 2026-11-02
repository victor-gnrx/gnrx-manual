---
description: Tire do estoque uma quantidade avariada ou perdida.
icon: minus
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

# Fazer uma baixa manual

**Para que serve:** tirar do estoque uma quantidade que não vai ser entregue (ex.: avaria detectada no almoxarifado).

{% hint style="info" %}
**Quem pode fazer:** Administrador, com a permissão de gerenciar o estoque de EPIs.
{% endhint %}

## Antes de começar

* Abra o item.

## Passo a passo

{% stepper %}
{% step %}
### Abra a baixa

No item, clique em **Baixa manual**. Abre **Baixa Manual de Estoque**.

<figure><img src="../../.gitbook/assets/inventario-baixa-01.png" alt="Janela Baixa Manual de Estoque com a quantidade e o motivo"><figcaption><p>Baixa Manual de Estoque</p></figcaption></figure>
{% endstep %}

{% step %}
### Confirme

Informe a quantidade e o motivo (ex.: avaria detectada no almoxarifado). Clique em **Confirmar baixa**. Aparece "Baixa registrada": "O estoque foi atualizado com sucesso.".
{% endstep %}
{% endstepper %}

## Deu errado?

| Mensagem na tela | O que fazer |
| --- | --- |
| "Informe a quantidade" | Preencha a quantidade. |
| "Quantidade deve ser maior que 0" | Ajuste a quantidade. |

## Dúvidas comuns

<details>

<summary>Como exporto as movimentações?</summary>

Use **Ações › Relatórios** e exporte as movimentações.

</details>

<details>

<summary>E se o EPI foi perdido por um colaborador?</summary>

Registre a perda na devolução do colaborador.

</details>
