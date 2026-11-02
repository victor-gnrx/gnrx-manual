---
description: Defina quando e para quem avisar sobre documentos vencendo.
icon: bell
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

# Configurar os alertas de vencimento

**Para que serve:** definir quando e para quem o GNRx avisa sobre documentos vencendo ou vencidos.

{% hint style="info" %}
**Quem pode fazer:** Gestor ou Administrador, com a permissão de editar alertas e política de bloqueio documental.
{% endhint %}

## Antes de começar

* A **Regra geral** vale para todo tipo de documento sem regra própria.

## Passo a passo

{% stepper %}
{% step %}
### Diga quando avisar

Clique em **Configurações › Alertas**. Em **Quando avisar**, informe os dias **Antes do vencimento** e **Depois de vencido**. Se quiser, ligue **Avisar também no dia do vencimento**.

<figure><img src="../.gitbook/assets/docs-alertas-01.png" alt="Tela Alertas de vencimento com Quando avisar, Quem recebe e as regras por tipo"><figcaption><p>Alertas de vencimento</p></figcaption></figure>
{% endstep %}

{% step %}
### Diga quem recebe

Em **Quem recebe**, marque o **Responsável pelo documento**, os **E-mails da unidade**, os usuários do portal da contratada e **O próprio colaborador** (notificação no app). Escolha os canais e salve. Aparece "Alertas salvos.".
{% endstep %}
{% endstepper %}

## Dúvidas comuns

<details>

<summary>Um tipo de documento precisa de outro aviso.</summary>

Em **Regras por tipo de documento**, use **Criar regra para um tipo…**.

</details>

<details>

<summary>Como aviso por WhatsApp?</summary>

Em **WhatsApp**, informe o **Template de vencimento aprovado na Meta** (ex.: vencimento_documento) e salve.

</details>
