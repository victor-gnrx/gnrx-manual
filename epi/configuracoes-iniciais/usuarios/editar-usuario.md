---
description: Corrija os dados de um usuário ou troque a senha dele.
icon: user-pen
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

# Editar um usuário

**Para que serve:** corrigir os dados de um usuário ou trocar a senha dele.

{% hint style="info" %}
**Quem pode fazer:** Administrador, com a permissão de editar usuários.
{% endhint %}

## Antes de começar

* O usuário precisa estar cadastrado. Se não estiver, veja [Criar um usuário](criar-usuario.md).

## Passo a passo

{% stepper %}
{% step %}
### Encontre o usuário

Clique em **Estruturas › Usuários**. Digite em **Pesquisar usuários...** o nome, o usuário, o e-mail ou o telefone.

<figure><img src="../../.gitbook/assets/usuarios-editar-01.png" alt="Lista de usuários filtrada pelo campo Pesquisar usuários"><figcaption><p>Pesquisa de usuários</p></figcaption></figure>
{% endstep %}

{% step %}
### Abra o usuário

Clique no usuário na lista. Abre o detalhe, com os cartões **Informações do Usuário**, **Alterar Senha**, **Unidades de Trabalho**, **Permissões de Módulos** e **Roles Atribuídas**.

<figure><img src="../../.gitbook/assets/usuarios-editar-02.png" alt="Detalhe do usuário com os cartões Informações do Usuário, Alterar Senha, Unidades de Trabalho, Permissões de Módulos e Roles Atribuídas"><figcaption><p>Detalhe do usuário</p></figcaption></figure>
{% endstep %}

{% step %}
### Corrija os dados

No cartão **Informações do Usuário**, abra a edição. Na janela **Atualizar usuário do sistema**, corrija o que precisar e salve. Aparece **Atualizado com sucesso!**.

<figure><img src="../../.gitbook/assets/usuarios-editar-03.png" alt="Janela Atualizar usuário do sistema com os dados do usuário"><figcaption><p>Janela Atualizar usuário do sistema</p></figcaption></figure>
{% endstep %}

{% step %}
### Troque a senha (se precisar)

No cartão **Alterar Senha**, digite a nova senha e salve. Aparece **Senha alterada com sucesso!**.

A senha precisa ter no mínimo 8 caracteres, com letra maiúscula, letra minúscula e número.

<figure><img src="../../.gitbook/assets/usuarios-editar-04.png" alt="Cartão Alterar Senha preenchido"><figcaption><p>Cartão Alterar Senha</p></figcaption></figure>
{% endstep %}
{% endstepper %}

## Deu errado?

{% hint style="warning" %}
**"Não é possível alterar a senha de um parceiro."**: usuários com o selo **Parceiro** não podem ter a senha trocada aqui.
{% endhint %}

## Dúvidas comuns

<details>

<summary>A pessoa esqueceu a senha. Preciso trocar por ela?</summary>

Não precisa. Ela mesma pode criar uma nova pela [recuperação de senha](../../acesso/esqueci-minha-senha.md).

</details>

<details>

<summary>Posso mudar o login do usuário?</summary>

O login é único em toda a GNRx. Se o novo já existir, aparece **"Esse nome de usuário já está em uso."**.

</details>
