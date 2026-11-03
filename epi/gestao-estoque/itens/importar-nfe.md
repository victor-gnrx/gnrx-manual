---
description: Dê entrada no estoque pelo XML da nota fiscal eletrônica.
icon: file-import
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

# Importar estoque pela NF-e

**Para que serve:** dar entrada no estoque direto do XML da nota fiscal eletrônica.

{% hint style="info" %}
**Quem pode fazer:** Administrador, com a permissão de gerenciar o estoque de EPIs.
{% endhint %}

## Antes de começar

* Tenha o arquivo .xml da NF-e (até 50 MB).

## Passo a passo

{% stepper %}
{% step %}
### Envie o XML

Clique em **Inventário › Gerenciar Inventário** e em **Ações › Importar via NF-e XML**. Arraste o XML e clique em **Analisar NF-e**.

<figure><img src="../../.gitbook/assets/inventario-nfe-01.png" alt="Revisão da NF-e com o número da nota, o emitente e itens não identificados com os campos Item do sistema e Centro de estoque"><figcaption><p>Revisão da NF-e</p></figcaption></figure>
{% endstep %}

{% step %}
### Revise

Em **Revisão da NF-e**, confira o **Nº da NF**, o **Emitente** e os **Itens**. Escolha o **Centro de estoque para todos** (ou um por item).

O item da nota que o GNRx não reconheceu aparece como **não identificado**. Em **Item do sistema**, busque e escolha o item correspondente. Se quiser, informe o **Nº do lote**. Enquanto houver itens pendentes, o rodapé mostra quantos faltam.
{% endstep %}

{% step %}
### Importe

Clique em **Importar** (o botão mostra quantos itens). Aparece **Importação concluída** (ou **Concluído com erros**, com a lista de erros).
{% endstep %}
{% endstepper %}

## Deu errado?

| Mensagem na tela | O que fazer |
| --- | --- |
| "Selecione um arquivo XML da NF-e" | Envie o arquivo .xml. |
| "Arquivo muito grande (máx. 50MB)" | Use o XML da nota. |
| **Importação falhou** | Confira o arquivo e tente de novo. |

## Dúvidas comuns

<details>

<summary>Errei o arquivo.</summary>

Clique em **Trocar arquivo**.

</details>

<details>

<summary>Concluído com erros. E agora?</summary>

Veja os **Erros:** e dê entrada à mão nos itens que falharam.

</details>
