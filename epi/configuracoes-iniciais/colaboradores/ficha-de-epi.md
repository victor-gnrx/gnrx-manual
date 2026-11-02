---
description: Gere a ficha de EPI do colaborador em PDF ou por QR Code.
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

# Gerar a ficha de EPI

**Para que serve:** gerar a ficha de EPI do colaborador em PDF, ou um QR Code que abre a ficha.

{% hint style="info" %}
**Quem pode fazer:** qualquer usuário com o módulo Gestão de EPIs.
{% endhint %}

## Antes de começar

* Abra o colaborador: **Estruturas › Colaboradores**, menu da coluna **Ações**, **Visualizar**.

## Passo a passo

{% stepper %}
{% step %}
### Abra a ficha

Clique em **Ficha EPI**.

<figure><img src="../../.gitbook/assets/colaboradores-ficha-01.png" alt="Janela da ficha de EPI com Unidade, as opções da ficha, o Período de entrega e o botão Gerar PDF"><figcaption><p>Ficha de EPI</p></figcaption></figure>
{% endstep %}

{% step %}
### Escolha a unidade e as opções

Em **Unidade**, escolha a unidade ou **Geral**. Unidade com "(customizado)" tem ficha própria. Se quiser, marque **Exibir hash de verificação**, **Incluir movimentação de setor** e **Incluir movimentação de cargo**, e limite o **Período de entrega** (**De** / **Até**).
{% endstep %}

{% step %}
### Gere o PDF

Clique em **Gerar PDF**. Aparece "Ficha de EPI gerada com sucesso" e o arquivo abre em uma nova aba.
{% endstep %}
{% endstepper %}

{% hint style="info" %}
**QR Code:** na aba **QR Code**, clique em **Gerar QR Code**. O QR Code é vitalício. Use **Baixar PNG** ou **Imprimir**. Quem escaneia vê a ficha.
{% endhint %}

## Dúvidas comuns

<details>

<summary>E os itens que não são EPI?</summary>

Clique em **Ficha Produto** e depois em **Gerar Ficha**. Aparece "Ficha de Produto gerada com sucesso".

</details>

<details>

<summary>Como mudo o logo e o CNPJ da ficha?</summary>

Na unidade. Veja [Configurar a unidade no EPI](../unidades/configuracoes-epi.md).

</details>
