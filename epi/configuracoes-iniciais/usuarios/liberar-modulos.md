---
description: Ligue ou desligue os módulos que um usuário pode usar.
icon: toggle-on
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

# Liberar módulos para um usuário

**Para que serve:** ligar ou desligar os módulos que o usuário pode usar.

{% hint style="info" %}
**Quem pode fazer:** Administrador, com a permissão de editar usuários.
{% endhint %}

## Antes de começar

* O módulo precisa ter sido contratado pela sua empresa.

## Passo a passo

{% stepper %}
{% step %}
### Abra o usuário

Clique em **Estruturas › Usuários**. Na coluna **Ações** do usuário, clique no ícone de olho.
{% endstep %}

{% step %}
### Ligue ou desligue os módulos

No cartão **Permissões de Módulos**, clique em **Editar**. Ligue ou desligue cada módulo. O DDS (Diálogo Diário de Segurança) também aparece aqui.

<figure><img src="../../.gitbook/assets/usuarios-modulos-01.png" alt="Cartão Permissões de Módulos em edição, com módulos ligados, desligados e um marcado como Indisponível"><figcaption><p>Permissões de módulos</p></figcaption></figure>
{% endstep %}

{% step %}
### Salve

Clique em **Salvar**. Aparece **Permissões atualizadas com sucesso!**.
{% endstep %}
{% endstepper %}

{% hint style="info" %}
A pessoa só acessa um módulo se a empresa contratou **e** o módulo está ligado no cadastro dela.
{% endhint %}

## Deu errado?

{% hint style="warning" %}
**O módulo aparece como "Indisponível" e não liga**: a sua empresa não contratou esse módulo.
{% endhint %}

## Dúvidas comuns

<details>

<summary>A pessoa vê "O usuário não possui permissão para acessar nenhum módulo." ao entrar. Por quê?</summary>

Nenhum módulo está ligado no cadastro dela. Ligue pelo menos um.

</details>

<details>

<summary>Ligar o módulo já libera tudo dentro dele?</summary>

Não. O que a pessoa pode fazer dentro do módulo depende da role. Veja [Entender as roles](o-que-sao-roles.md).

</details>
