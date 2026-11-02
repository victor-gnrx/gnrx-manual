---
description: "Registre a devolução de um EPI entregue."
icon: rotate-left
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

# Registrar uma devolução

**Para que serve:** registrar que o colaborador devolveu o EPI, e para onde ele vai (estoque, manutenção, higienização).

{% hint style="info" %}
**Quem pode fazer:** Supervisor, Gestor ou Administrador, com a permissão de processar devolução de EPIs.
{% endhint %}

## Antes de começar

* O EPI precisa estar entregue e assinado.

## Passo a passo

{% stepper %}
{% step %}
### Abra a devolução

Abra a solicitação e clique em **Efetuar Devolução**.

<figure><img src="../../.gitbook/assets/devolucao-registrar-01.png" alt="Formulário de devolução com o Tipo de movimentação, a data, o motivo e o destino"><figcaption><p>Efetuar Devolução</p></figcaption></figure>
{% endstep %}

{% step %}
### Preencha

Em **Tipo de movimentação**, escolha **Devolução**. Informe a **Data de Devolução** e o **Motivo da Devolução**. Diga o destino do item: **Descartar**, **Manutenção** ou **Higienização** (com a **Lavanderia**, o **Retorno previsto** e o **Custo da lavagem**). Clique em **Confirmar**. Aparece "Devolução efetuada com sucesso.".
{% endstep %}
{% endstepper %}

## Deu errado?

| Mensagem na tela | O que fazer |
| --- | --- |
| "O EPI precisa ser entregue antes de iniciar o processo de devolução." | Efetue a entrega primeiro. |
| "Antes de devolver o EPI, é necessário assinar todos os itens." | Colha a assinatura. |
| "Não há itens disponíveis para devolução." | Nada a devolver nesta solicitação. |
| "Não existem motivos cadastrados para devolução" | Cadastre um [motivo de devolução](../../configuracoes-gerais/motivos/motivos-devolucao.md). |

## Dúvidas comuns

<details>

<summary>E se o EPI foi perdido ou quebrou?</summary>

Veja [Registrar perda](registrar-perda.md) e [Registrar quebra](registrar-quebra.md).

</details>

<details>

<summary>O item é descartável.</summary>

Itens **Sem devolução** não aparecem no painel de devoluções.

</details>
