---
description: "Registre que um EPI entregue foi quebrado."
icon: hammer
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

# Registrar uma quebra

**Para que serve:** registrar que o colaborador não vai devolver o EPI porque ele foi quebrado.

{% hint style="info" %}
**Quem pode fazer:** Supervisor, Gestor ou Administrador, com a permissão de processar devolução de EPIs.
{% endhint %}

## Antes de começar

* O EPI precisa estar entregue e assinado.
* Cadastre os [motivos de quebra](../../configuracoes-gerais/motivos/motivos-quebra.md).

## Passo a passo

{% stepper %}
{% step %}
### Abra a devolução

Abra a solicitação e clique em **Efetuar Devolução**.

<figure><img src="../../.gitbook/assets/devolucao-quebra-01.png" alt="Formulário de devolução com Tipo de movimentação Quebra, a data e o motivo"><figcaption><p>Quebra</p></figcaption></figure>
{% endstep %}

{% step %}
### Preencha

Em **Tipo de movimentação**, escolha **Quebra**. Informe a **Data da Quebra** e o **Motivo da Quebra**. Se quiser, escreva as **Observações**. Clique em **Confirmar**.
{% endstep %}
{% endstepper %}

## Deu errado?

| Mensagem na tela | O que fazer |
| --- | --- |
| "Não existem motivos cadastrados para quebra" | Cadastre um [motivo de quebra](../../configuracoes-gerais/motivos/motivos-quebra.md). |
| "Preencha todos os campos necessários para o tipo selecionado" | Preencha a data e o motivo. |
| "Antes de devolver o EPI, é necessário assinar todos os itens." | Colha a assinatura. |

## Dúvidas comuns

<details>

<summary>Como fica o item depois?</summary>

Ele aparece como **Reportado como Quebrado**.

</details>

<details>

<summary>Errei a data ou o motivo.</summary>

Abra a movimentação e clique em **Editar**.

</details>
