---
description: Configure o aplicativo autenticador ou o código por e-mail para entrar com segurança.
icon: shield-halved
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

# Configurar a verificação em duas etapas

**Para que serve:** cadastrar um segundo jeito de confirmar que é você no login: um aplicativo autenticador, o e-mail ou os dois.

{% hint style="info" %}
**Quem pode fazer:** qualquer usuário, em **Meu Perfil**, e o acesso Empresa, em **Minha Empresa**.
{% endhint %}

## Antes de começar

* Para usar um aplicativo, instale um aplicativo autenticador no celular (Google Authenticator, Authy etc.).

## Passo a passo

{% stepper %}
{% step %}
### Abra a segurança

* No acesso Usuário: menu do usuário, **Meu Perfil › Segurança**. Abre **Configurações de Segurança**.
* No acesso Empresa: menu do usuário, **Minha Empresa › Segurança**. Os seus fatores ficam em **Seus fatores de verificação**.

<figure><img src="../.gitbook/assets/mfa-01-seguranca.png" alt="Seção Configurações de Segurança com as opções Aplicativo autenticador (TOTP) e Código por e-mail"><figcaption><p>Configurações de Segurança</p></figcaption></figure>
{% endstep %}

{% step %}
### Configure o aplicativo autenticador

Em **Aplicativo autenticador (TOTP)**, clique em **Configurar aplicativo autenticador**. Abra o aplicativo no celular e escaneie o QR code. Digite os 6 dígitos que aparecem no aplicativo e clique em **Confirmar código**.

Não consegue escanear? Clique em **Não consigo escanear o QR code** e digite o código no aplicativo.

<figure><img src="../.gitbook/assets/mfa-02-qrcode.png" alt="Tela com o QR code para escanear, o link Não consigo escanear o QR code e o campo de 6 dígitos"><figcaption><p>QR code do aplicativo autenticador</p></figcaption></figure>
{% endstep %}

{% step %}
### Ou configure o código por e-mail

Em **Código por e-mail**, comece a configuração. Aparece "Enviamos um código de verificação para o seu e-mail". Digite o código para confirmar. A partir daí, você recebe um código a cada login.

<figure><img src="../.gitbook/assets/mfa-03-email.png" alt="Tela com a mensagem Enviamos um código de verificação para o seu e-mail e o campo do código"><figcaption><p>Código por e-mail</p></figcaption></figure>
{% endstep %}
{% endstepper %}

## Dúvidas comuns

<details>

<summary>Posso ter os dois?</summary>

Pode. No login, você escolhe qual usar.

</details>

<details>

<summary>Como tiro um dos dois?</summary>

Clique em **Remover** ao lado dele e confirme.

</details>

<details>

<summary>Sou obrigado a configurar?</summary>

Depende da sua empresa. Ela pode [exigir a verificação](../minha-empresa/exigir-verificacao.md) para o acesso Empresa e para algumas roles.

</details>
