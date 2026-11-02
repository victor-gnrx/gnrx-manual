---
description: No EPI, cadastre quem recebe os avisos de cada unidade.
icon: envelope
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

# Cadastrar os e-mails da unidade

**Para que serve:** definir quem recebe os avisos de cada unidade, como estoque mínimo, compras e validade.

{% hint style="info" %}
**Quem pode fazer:** quem abre a unidade no módulo Gestão de EPIs.
{% endhint %}

## Antes de começar

* Tenha a lista de e-mails da unidade.

## Passo a passo

{% stepper %}
{% step %}
### Abra a unidade

Clique em **Estruturas › Unidades**. Na coluna **Ações**, clique no ícone de olho. Na aba **Visão Geral**, vá aos e-mails da unidade.
{% endstep %}

{% step %}
### Adicione o e-mail

Digite o e-mail (ex.: novo@email.com) e clique em **Adicionar**. Aparece "Email adicionado com sucesso".

<figure><img src="../../.gitbook/assets/unidades-emails-01.png" alt="Lista de e-mails da unidade com o campo de e-mail e o botão Adicionar"><figcaption><p>E-mails da unidade</p></figcaption></figure>
{% endstep %}

{% step %}
### Escolha o que ele recebe

Clique no e-mail. Na aba **Módulos**, ligue os **Módulos Ativos**. Na aba **Notificações EPI**, escolha **Alertas de Estoque Mínimo**, **Solicitações de Compra** e **Validade do Fabricante**. Em **Notificações por Setor**, ligue por setor **Devoluções** e **Solicitações de EPI**. Clique em **Salvar Notificações EPI**.

<figure><img src="../../.gitbook/assets/unidades-emails-02.png" alt="Janela do e-mail com as abas Módulos e Notificações EPI"><figcaption><p>Módulos e notificações do e-mail</p></figcaption></figure>
{% endstep %}
{% endstepper %}

## Deu errado?

{% hint style="warning" %}
**"Email inválido"**: confira o e-mail digitado.
{% endhint %}

## Dúvidas comuns

<details>

<summary>Como tiro um e-mail?</summary>

Clique em **Remover email** e confirme em **Remover**. Aparece "Email removido com sucesso".

</details>

<details>

<summary>Qual a diferença para os E-mails SESMT?</summary>

Os [E-mails SESMT](../../minha-empresa/emails-sesmt.md) valem para a empresa toda. Os daqui valem só para esta unidade.

</details>
