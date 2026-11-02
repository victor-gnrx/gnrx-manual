---
description: Dê acesso ao GNRx a uma pessoa nova.
icon: user-plus
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

# Criar um usuário

**Para que serve:** dar acesso ao GNRx a uma pessoa nova.

{% hint style="info" %}
**Quem pode fazer:** Administrador, com a permissão de criar usuários.
{% endhint %}

## Antes de começar

* Cadastre a [unidade](../unidades/README.md) onde a pessoa trabalha.
* Escolha a role da pessoa. Se tiver dúvida, veja [Entender as roles](o-que-sao-roles.md).

## Passo a passo

{% stepper %}
{% step %}
### Abra a tela de usuários

Dentro de qualquer módulo, clique em **Estruturas › Usuários**. Abre a tela **Usuários do Sistema**.

<figure><img src="../../.gitbook/assets/usuarios-criar-01.png" alt="Tela Usuários do Sistema com a lista de usuários e o botão Novo usuário"><figcaption><p>Tela Usuários do Sistema</p></figcaption></figure>
{% endstep %}

{% step %}
### Clique em Novo usuário

Clique em **Novo usuário**. Abre a janela **Criar usuário**.

<figure><img src="../../.gitbook/assets/usuarios-criar-02.png" alt="Janela Criar usuário aberta, com a seção Informações Pessoais"><figcaption><p>Janela Criar usuário</p></figcaption></figure>
{% endstep %}

{% step %}
### Preencha as informações pessoais

* **Usuário (Login):** de 3 a 255 caracteres. Use só letras, números, ponto e sublinhado.
* **Nome Completo:** de 3 a 100 caracteres.
* **CPF (Opcional)**, **Data de Nascimento**, **Email**, **Telefone** e **Endereço**.
* **Senha:** no mínimo 8 caracteres, com letra maiúscula, letra minúscula e número.

{% hint style="info" %}
Aqui a senha não precisa de caractere especial. Só a [recuperação por e-mail](../../acesso/esqueci-minha-senha.md) exige.
{% endhint %}

<figure><img src="../../.gitbook/assets/usuarios-criar-03.png" alt="Seção Informações Pessoais preenchida com usuário, nome, e-mail e senha"><figcaption><p>Informações pessoais preenchidas</p></figcaption></figure>
{% endstep %}

{% step %}
### Escolha a role e as unidades

Em **Role Inicial / Permissão**, escolha a role. Ela é obrigatória.

Em **Unidades**, marque onde a pessoa trabalha.

{% hint style="warning" %}
Marque sempre pelo menos uma unidade. Sem unidade, a pessoa não vê os registros na maioria das telas.
{% endhint %}

<figure><img src="../../.gitbook/assets/usuarios-criar-04.png" alt="Campos Role Inicial / Permissão e Unidades preenchidos"><figcaption><p>Role e unidades</p></figcaption></figure>
{% endstep %}

{% step %}
### Ligue os módulos e salve

Em **Módulos de Acesso**, ligue os módulos que a pessoa vai usar: Formulários, Auditorias, Gestão de EPIs, Gestão de Treinamentos, Gestão de Documentos, Gestão de CIPA ou Gestão de Acidentes.

Salve. Aparece **Usuário criado com sucesso**.

<figure><img src="../../.gitbook/assets/usuarios-criar-05.png" alt="Seção Módulos de Acesso com alguns módulos ligados"><figcaption><p>Módulos de acesso</p></figcaption></figure>
{% endstep %}
{% endstepper %}

## Deu errado?

{% hint style="warning" %}
**"Esse nome de usuário já está em uso."**: o login é único em toda a GNRx, não só na sua empresa. Escolha outro.
{% endhint %}

{% hint style="warning" %}
**"Acesso Negado: Você não tem permissão para acessar esta página"**: você não pode ver usuários. Peça a um Administrador.
{% endhint %}

## Dúvidas comuns

<details>

<summary>Dois usuários podem ter o mesmo CPF ou e-mail?</summary>

Podem. Só o login não pode se repetir.

</details>

<details>

<summary>A pessoa pode entrar com o CPF?</summary>

Pode, se o CPF estiver no cadastro. Veja [Entrar no sistema](../../acesso/entrar-no-sistema.md).

</details>

<details>

<summary>Esqueci de marcar a unidade. E agora?</summary>

Você pode marcar depois. Veja [Vincular unidades a um usuário](vincular-unidades.md).

</details>
