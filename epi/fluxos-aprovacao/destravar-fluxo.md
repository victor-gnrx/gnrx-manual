---
description: Reatribua as etapas que travaram sem aprovador.
icon: unlock
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

# Destravar um fluxo

**Para que serve:** reatribuir as etapas de fluxos que travaram sem aprovador, para a solicitação seguir.

{% hint style="info" %}
**Quem pode fazer:** Gestor ou Administrador, com a permissão de reatribuir etapas de fluxos que travaram sem aprovador.
{% endhint %}

## Antes de começar

* Nada a preparar.

## Passo a passo

{% stepper %}
{% step %}
### Abra os travados

Clique em **Configurações › Fluxos Travados**.

<figure><img src="../.gitbook/assets/fluxos-travados-01.png" alt="Tela Fluxos travados com a lista e os botões Ver solicitação, Ver o fluxo e Reatribuir"><figcaption><p>Fluxos travados</p></figcaption></figure>
{% endstep %}

{% step %}
### Reatribua

Use **Ver solicitação** ou **Ver o fluxo** para entender. Clique em **Reatribuir** e escolha os novos aprovadores da etapa. Aparece **Etapa reatribuída**: "O fluxo voltou a andar e já aparece para os novos aprovadores."
{% endstep %}
{% endstepper %}

## Deu errado?

| Mensagem na tela | O que fazer |
| --- | --- |
| "Esta instância não está travada" | Alguém já destravou. Atualize a lista. |
| "Não foi possível reatribuir" | Tente de novo. |

## Dúvidas comuns

<details>

<summary>Apareceu "Nenhum fluxo travado."</summary>

Todas as etapas têm aprovador.

</details>

<details>

<summary>Por que um fluxo trava?</summary>

Quando a etapa fica sem aprovador apto (ex.: o supervisor saiu). No editor, a etapa de supervisor tem a opção **Quando não há supervisor apto**.

</details>
