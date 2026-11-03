---
description: "Gere o PDF da auditoria e baixe as fotos e os documentos."
icon: file-pdf
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

# Emitir o relatório da auditoria

**Para que serve:** gerar o PDF da auditoria para enviar ou arquivar, e baixar as fotos e os documentos anexados.

{% hint style="info" %}
**Quem pode fazer:** todas as roles, com a permissão de exportar relatórios de auditoria.
{% endhint %}

## Antes de começar

* [Preencha a auditoria](preencher-auditoria.md).

## Passo a passo

{% stepper %}
{% step %}
### Abra o relatório

Abra a auditoria e clique em **Relatório**.

<figure><img src="../.gitbook/assets/aud-relatorio-01.png" alt="Relatório da auditoria com o botão Emitir Relatório PDF e os botões de baixar fotos e documentos"><figcaption><p>Relatório da auditoria</p></figcaption></figure>
{% endstep %}

{% step %}
### Configure

Clique em **Emitir Relatório PDF**. Em **Exibição**, marque **Data e hora dos itens** se quiser mostrar quando cada item foi respondido. Clique em **Gerar PDF**.
{% endstep %}

{% step %}
### Aguarde

Não feche a janela até o PDF ficar pronto.
{% endstep %}

{% step %}
### Abra o PDF

Clique em **Abrir PDF**. O link vale por 1 hora.

<figure><img src="../.gitbook/assets/aud-relatorio-02.png" alt="Janela Relatório Gerado com o botão Abrir PDF e o aviso de link válido por 1 hora"><figcaption><p>Relatório Gerado</p></figcaption></figure>
{% endstep %}
{% endstepper %}

## Deu errado?

{% hint style="warning" %}
**"Não foi possível gerar o relatório."**: clique em **Tentar novamente**.
{% endhint %}

{% hint style="warning" %}
**"Não foi possível iniciar a geração. Tente novamente."**: clique em **Emitir Relatório PDF** de novo.
{% endhint %}

## Dúvidas comuns

<details>

<summary>O link expirou?</summary>

Gere o PDF de novo. Por segurança, os links valem 1 hora. Os gerados aparecem em **Relatórios gerados**.

</details>

<details>

<summary>Como baixo todas as fotos?</summary>

Na página do relatório, clique em **Baixar fotos**. Para os anexos, clique em **Baixar documentos**.

</details>
