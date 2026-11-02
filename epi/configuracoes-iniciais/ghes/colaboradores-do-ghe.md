---
description: Coloque ou tire colaboradores de um GHE.
icon: users
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

# Adicionar colaboradores a um GHE

**Para que serve:** colocar as pessoas no grupo. Quem está no GHE recebe os EPIs exigidos pelos riscos dele.

{% hint style="info" %}
**Quem pode fazer:** Gestor ou Administrador, com a permissão de associar EPIs aos GHEs.
{% endhint %}

## Antes de começar

* Os colaboradores precisam estar na unidade do GHE.

## Passo a passo

{% stepper %}
{% step %}
### Abra os colaboradores

No GHE, abra a aba **Colaboradores** e clique em **Adicionar Colaboradores**. Abre **Selecionar Colaboradores**.

<figure><img src="../../.gitbook/assets/ghe-colaboradores-01.png" alt="Painel Selecionar Colaboradores com a busca, Selecionar Todos e o botão Associar"><figcaption><p>Selecionar Colaboradores</p></figcaption></figure>
{% endstep %}

{% step %}
### Marque e associe

Use **Pesquisar colaboradores...**, marque as pessoas (ou **Selecionar Todos**) e clique em **Associar**. Aparece "N colaboradores associados ao GHE.".
{% endstep %}
{% endstepper %}

{% hint style="info" %}
**Para tirar alguém:** na aba **Colaboradores**, marque quem sai do GHE e clique em **Remover**. Confirme em **Remover do GHE?**. A pessoa deixa de receber os EPIs exigidos pelo GHE. As entregas já feitas continuam na ficha.
{% endhint %}

## Deu errado?

{% hint style="warning" %}
**"Associação parcial"**: parte dos colaboradores não foi associada. Confira se eles estão na unidade do GHE.
{% endhint %}

## Dúvidas comuns

<details>

<summary>Apareceu "Todos os colaboradores já estão no GHE".</summary>

Não há mais ninguém para adicionar.

</details>

<details>

<summary>Como vejo quem está sem EPI obrigatório?</summary>

Na aba **Colaboradores**, quem está sem EPI aparece com o aviso (ex.: "Falta 1 EPI"). Se aparecer "Ninguém sem EPI obrigatório. Tudo em dia.", está tudo certo.

</details>
