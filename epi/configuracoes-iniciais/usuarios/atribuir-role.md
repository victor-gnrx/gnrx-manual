---
description: Dê a um usuário as permissões de uma role.
icon: user-tag
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

# Atribuir uma role a um usuário

**Para que serve:** dar a um usuário as permissões de uma role.

{% hint style="info" %}
**Quem pode fazer:** Administrador, com a permissão de gerenciar roles de usuários.
{% endhint %}

## Antes de começar

* Escolha a role. Veja [Entender as roles](o-que-sao-roles.md). Se nenhuma servir, [crie uma role](criar-role.md).

## Passo a passo

{% stepper %}
{% step %}
### Abra o usuário

Clique em **Estruturas › Usuários**. Na coluna **Ações** do usuário, clique no ícone de olho.
{% endstep %}

{% step %}
### Adicione a role

No cartão **Roles Atribuídas**, clique em **Adicionar Nova Role**. Escolha a role e clique em **Adicionar**. Aparece **Role adicionada com sucesso!**.

<figure><img src="../../.gitbook/assets/usuarios-role-01.png" alt="Cartão Roles Atribuídas com a escolha de uma nova role e o botão Adicionar"><figcaption><p>Adicionar nova role</p></figcaption></figure>
{% endstep %}
{% endstepper %}

{% hint style="info" %}
**Outro caminho:** em **Configurações › Roles & Permissões**, abra a role e clique em **Adicionar Usuário**. Deixe **Unidade** e **Setor** como Global. Quem limita o que a pessoa vê são as [unidades vinculadas ao usuário](vincular-unidades.md).
{% endhint %}

## Deu errado?

{% hint style="warning" %}
**"Acesso Restrito: Você não tem permissão para gerenciar roles"**: só o Administrador atribui roles.
{% endhint %}

## Dúvidas comuns

<details>

<summary>E se o usuário tiver duas roles?</summary>

As permissões se somam. Se qualquer uma delas exigir verificação em duas etapas, o código passa a ser pedido no login.

</details>

<details>

<summary>A role muda o que a pessoa vê?</summary>

A role muda o que ela pode **fazer**. O que ela **vê** depende das [unidades](vincular-unidades.md) e dos [módulos](liberar-modulos.md) dela.

</details>
