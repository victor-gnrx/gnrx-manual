---
description: Diga a que riscos os colaboradores do GHE estão expostos.
icon: triangle-exclamation
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

# Vincular riscos a um GHE

**Para que serve:** dizer a que riscos o grupo está exposto. Os riscos dizem quais EPIs o grupo precisa.

{% hint style="info" %}
**Quem pode fazer:** Gestor ou Administrador, com a permissão de associar EPIs aos GHEs.
{% endhint %}

## Antes de começar

* [Crie o GHE](criar-ghe.md).

## Passo a passo

{% stepper %}
{% step %}
### Abra os riscos

No GHE, abra a aba **Riscos / EPIs** e clique em **Gerenciar riscos**. Abre **Riscos deste GHE**: "Marque os riscos a que o grupo está exposto.".

<figure><img src="../../.gitbook/assets/ghe-riscos-01.png" alt="Janela Riscos deste GHE com a busca e a lista de riscos para marcar"><figcaption><p>Riscos deste GHE</p></figcaption></figure>
{% endstep %}

{% step %}
### Marque e salve

Use **Buscar por nome ou descrição** para achar o risco. Marque os riscos e clique em **Salvar**. Aparece "Riscos do GHE atualizados.".
{% endstep %}
{% endstepper %}

Depois, [escolha os EPIs de cada risco](vincular-epis.md).

## Dúvidas comuns

<details>

<summary>O risco não aparece na lista.</summary>

Ele precisa estar cadastrado em **Configurações › Riscos**.

</details>

<details>

<summary>Dá para copiar os riscos de outro GHE?</summary>

Dá. Veja [Copiar a configuração de outro GHE](copiar-configuracoes.md).

</details>
