---
description: Acesse o GNRx com o seu usuário, o CPF ou o CNPJ da empresa.
icon: right-to-bracket
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

# Entrar no sistema

**Para que serve:** acessar o GNRx com o seu usuário ou com o acesso mestre da empresa.

{% hint style="info" %}
**Quem pode fazer:** qualquer pessoa com usuário cadastrado no GNRx (Operador, Supervisor, Gestor ou Administrador). A aba **Empresa** é para quem tem o CNPJ e a senha mestre da empresa.
{% endhint %}

## Antes de começar

* Tenha em mãos o seu usuário (ou CPF) e a senha. Se esqueceu a senha, veja [Recuperar a senha](esqueci-minha-senha.md).
* Se a sua conta usa verificação em duas etapas, deixe o seu e-mail ou o seu aplicativo autenticador por perto.

## Passo a passo

{% stepper %}
{% step %}
### Abra a tela de login

Abra o GNRx no navegador. A tela mostra **Acesse sua conta**.

<figure><img src=".gitbook/assets/login-01-tela.png" alt="Tela de login do GNRx com o título Acesse sua conta e as abas Usuário e Empresa"><figcaption><p>Tela de login</p></figcaption></figure>
{% endstep %}

{% step %}
### Preencha usuário e senha

Na aba **Usuário**, digite o seu usuário ou CPF no campo **Usuário**, depois a **Senha**. Clique em **Entrar**.

<figure><img src=".gitbook/assets/login-02-aba-usuario-preenchida.png" alt="Aba Usuário com os campos Usuário e Senha preenchidos e o botão Entrar"><figcaption><p>Aba Usuário preenchida</p></figcaption></figure>

{% hint style="info" %}
**Acesso da empresa:** na aba **Empresa**, digite o **CNPJ** e a **Senha** da empresa. Esse acesso vê tudo da empresa.
{% endhint %}

<figure><img src=".gitbook/assets/login-03-aba-empresa.png" alt="Aba Empresa com os campos CNPJ e Senha"><figcaption><p>Aba Empresa</p></figcaption></figure>
{% endstep %}

{% step %}
### Digite o código de verificação (se pedir)

Se aparecer **Verificação em duas etapas**, digite os 6 dígitos que chegaram no seu e-mail ou que aparecem no seu aplicativo autenticador. O sistema envia sozinho ao completar.

<figure><img src=".gitbook/assets/login-04-mfa.png" alt="Tela Verificação em duas etapas com seis campos para o código"><figcaption><p>Verificação em duas etapas</p></figcaption></figure>

* Não chegou? Clique em **Reenviar código** quando a contagem terminar.
* Para trocar o jeito de receber, clique em **Usar aplicativo autenticador** ou **Prefiro receber o código por e-mail**.
{% endstep %}

{% step %}
### Pronto

O GNRx abre o painel do primeiro módulo que a sua empresa contratou.

<figure><img src=".gitbook/assets/login-05-painel-apos-login.png" alt="Painel do módulo aberto logo após o login"><figcaption><p>Painel após o login</p></figcaption></figure>
{% endstep %}
{% endstepper %}

## Deu errado?

{% hint style="warning" %}
**"Sua sessão de verificação expirou..."**: você demorou para digitar o código. Clique em **Voltar para o login** e entre de novo.
{% endhint %}

## Dúvidas comuns

<details>

<summary>Posso entrar com o CPF?</summary>

Pode. Na aba **Usuário**, digite o CPF no campo **Usuário**.

</details>

<details>

<summary>Por que o sistema sempre pede o código?</summary>

Quem tem o perfil Administrador sempre passa pela verificação em duas etapas. Além disso, a empresa pode ligar **MFA obrigatório** numa role própria. Aí todos com essa role passam a receber o código.

</details>

<details>

<summary>Entrei e não vi o painel. Está errado?</summary>

Não. Se você não tem permissão para ver o painel, o GNRx abre uma tela de trabalho do módulo. No EPI, por exemplo, abre **Nova solicitação**.

</details>
