---
description: Aprove ou rejeite as solicitações que esperam a sua decisão.
icon: check-double
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

# Decidir uma aprovação

**Para que serve:** aprovar ou rejeitar as solicitações que estão esperando a sua decisão.

{% hint style="info" %}
**Quem pode fazer:** quem foi escolhido como aprovador na etapa, com a permissão de decidir as etapas de aprovação atribuídas a si (Supervisor, Gestor e Administrador).
{% endhint %}

## Antes de começar

* Nada a preparar.

## Passo a passo

{% stepper %}
{% step %}
### Abra Minhas aprovações

Clique em **Configurações › Minhas Aprovações**. Filtre por **Tipo de solicitação**, se quiser.

<figure><img src="../.gitbook/assets/fluxos-aprovacoes-01.png" alt="Tela Minhas aprovações com os cartões das solicitações e os botões Aprovar e Rejeitar"><figcaption><p>Minhas aprovações</p></figcaption></figure>
{% endstep %}

{% step %}
### Confira

Use **Abrir solicitação** para ver os detalhes ou **Ver o fluxo desta solicitação** para ver as etapas.
{% endstep %}

{% step %}
### Decida

Clique em **Aprovar** e em **Confirmar Aprovação**. Aparece "Etapa aprovada": a solicitação seguiu para a próxima etapa. Ou clique em **Rejeitar**, escreva o motivo (se a etapa exige) e clique em **Confirmar Rejeição**.
{% endstep %}
{% endstepper %}

{% hint style="warning" %}
Rejeitar encerra a solicitação inteira, inclusive as etapas paralelas pendentes.
{% endhint %}

## Deu errado?

| Mensagem na tela | O que fazer |
| --- | --- |
| "Você não está entre os aprovadores" | Esta etapa foi configurada para outras pessoas decidirem. |
| "Etapa já decidida" | Alguém decidiu antes ou o fluxo não está mais em andamento. |
| "Esta etapa exige um motivo para a rejeição." | Escreva o motivo. |

## Dúvidas comuns

<details>

<summary>Apareceu "Nada aguardando você por aqui."</summary>

Não há solicitação esperando a sua decisão.

</details>

<details>

<summary>Posso avisar o colaborador?</summary>

Se a etapa permitir, aparecem **Notificar via aplicativo** e **Notificar por email**.

</details>
