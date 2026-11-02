---
description: Tire da lista um GHE sem uso, ou traga de volta.
icon: ban
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

# Inativar ou reativar um GHE

**Para que serve:** tirar da lista um GHE que a empresa não usa mais, ou trazer de volta.

{% hint style="info" %}
**Quem pode fazer:** Gestor ou Administrador, com a permissão de inativar GHEs.
{% endhint %}

## Antes de começar

* Confira se o GHE é mesmo o certo. Use a [busca](listar-ghe.md).

## Passo a passo

{% stepper %}
{% step %}
### Inative

Clique em **Estruturas** e abra os GHEs (no módulo Gestão de EPIs, **Estruturas › GHEs — Grupos de EPIs**). Na coluna **Ações**, clique no ícone de lixeira. Abre **Inativar Grupo**: "Tem certeza que deseja inativar este Grupo?". Clique em **Inativar**. Aparece "Grupo excluído com sucesso!".

<figure><img src="../../.gitbook/assets/ghe-inativar-01.png" alt="Janela Inativar Grupo com a pergunta de confirmação"><figcaption><p>Inativar Grupo</p></figcaption></figure>
{% endstep %}

{% step %}
### Para reativar

Em **Filtrar por status**, escolha **Status: Inativo**. Na coluna **Ações**, use **Reativar grupo** e confirme. Aparece "Grupo reativado com sucesso!".
{% endstep %}
{% endstepper %}

## Dúvidas comuns

<details>

<summary>A mensagem diz "excluído". O GHE foi apagado?</summary>

Não. O GHE fica inativo e pode ser reativado.

</details>

<details>

<summary>Inativei uma unidade e os GHEs dela ficaram inativos.</summary>

É assim mesmo: ao inativar uma unidade, os GHEs dela são inativados junto.

</details>
