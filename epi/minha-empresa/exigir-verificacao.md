---
description: Ligue a verificação em duas etapas para a empresa e para as roles que exigem.
icon: lock
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

# Exigir a verificação em duas etapas

**Para que serve:** pedir um código, além da senha, no login da empresa e dos usuários com role marcada como **MFA obrigatório**.

{% hint style="info" %}
**Quem pode fazer:** só o acesso Empresa (CNPJ).
{% endhint %}

## Antes de começar

* Configure os fatores da própria empresa: [Configurar a verificação em duas etapas](../acesso/verificacao-em-duas-etapas.md).
* Decida quais roles exigem o código. Por padrão, só a role Administrador exige. Nas outras, ligue **MFA obrigatório** ao criar ou editar a role.

## Passo a passo

{% stepper %}
{% step %}
### Abra a aba Segurança

No menu do usuário, clique em **Minha Empresa** e depois na aba **Segurança**.
{% endstep %}

{% step %}
### Ligue a exigência

No cartão **Exigência de MFA para a empresa**, ligue **Exigir autenticação em duas etapas**.

<figure><img src="../.gitbook/assets/empresa-04-exigir-mfa.png" alt="Cartão Exigência de MFA para a empresa com a chave Exigir autenticação em duas etapas ligada"><figcaption><p>Exigir autenticação em duas etapas</p></figcaption></figure>
{% endstep %}

{% step %}
### Decida se bloqueia quem não configurou

Abra **Avançado** e ligue **Bloquear login sem fator configurado**, se quiser. Escolha **Bloquear imediatamente** ou **Dias de carência** e clique em **Salvar**.

<figure><img src="../.gitbook/assets/empresa-05-avancado.png" alt="Parte Avançado aberta com Bloquear login sem fator configurado, as opções Bloquear imediatamente e Dias de carência e o botão Salvar"><figcaption><p>Opções avançadas</p></figcaption></figure>
{% endstep %}
{% endstepper %}

## O que o usuário vê

| Situação | O que acontece no login |
| --- | --- |
| Exigência ligada, sem bloqueio | O usuário entra e é lembrado de configurar a verificação. |
| Com bloqueio, prazo vencido | Aparece "Configure a autenticação em duas etapas para continuar acessando..." e ele não entra. |

## Dúvidas comuns

<details>

<summary>Para que servem os dias de carência?</summary>

Dão um prazo para os usuários configurarem a verificação antes do bloqueio.

</details>

<details>

<summary>Um usuário foi bloqueado. Como ajudo?</summary>

Ele precisa configurar a verificação em **Meu Perfil › Segurança**. Mostre a ele [Configurar a verificação em duas etapas](../acesso/verificacao-em-duas-etapas.md).

</details>
