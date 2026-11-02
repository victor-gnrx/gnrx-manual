---
description: Diga a cada quantos dias trocar cada item para quem está no GHE.
icon: calendar-days
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

# Definir prazos de troca

**Para que serve:** dizer quando cada item deve ser trocado por quem está no GHE. Com prazo, o sistema avisa quando trocar.

{% hint style="info" %}
**Quem pode fazer:** Gestor ou Administrador, com a permissão de associar EPIs aos GHEs.
{% endhint %}

## Antes de começar

* [Escolha os EPIs](vincular-epis.md). Os itens aparecem aqui quando atendem algum EPI exigido pelo GHE.

## Passo a passo

{% stepper %}
{% step %}
### Abra os prazos

No GHE, abra a aba **Prazos de troca**. Cada item mostra de onde vem o prazo: **Definido neste GHE**, **Da unidade**, **Do cadastro do item** ou **Nem na unidade nem no item**.

<figure><img src="../../.gitbook/assets/ghe-prazos-01.png" alt="Aba Prazos de troca com a lista de itens, a origem do prazo de cada um e o filtro Só sem prazo"><figcaption><p>Prazos de troca</p></figcaption></figure>
{% endstep %}

{% step %}
### Defina o prazo

No item, escolha **Neste GHE** e informe **a cada** quantos **dias** (de 1 a 3650). Ou marque **Isento de troca**. Clique em **Salvar**. Aparece "Prazo de troca salvo para este GHE.".
{% endstep %}

{% step %}
### Volte ao prazo padrão (se quiser)

Escolha **Usar o da unidade**. O item volta a seguir o prazo da unidade ou do cadastro.
{% endstep %}
{% endstepper %}

{% hint style="info" %}
O prazo do GHE vale acima do da unidade e do cadastro do item.
{% endhint %}

## Dúvidas comuns

<details>

<summary>Como acho os itens sem prazo?</summary>

Use **Só sem prazo**. Se aparecer "Nenhum item sem prazo. Tudo certo por aqui.", todos têm prazo.

</details>

<details>

<summary>Apareceu "Informe de 1 a 3650 dias.".</summary>

O prazo precisa ficar entre 1 e 3650 dias.

</details>
