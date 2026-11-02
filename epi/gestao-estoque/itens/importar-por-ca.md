---
description: Cadastre muitos EPIs de uma vez por planilha, pelo CA.
icon: file-excel
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

# Importar itens por CA

**Para que serve:** cadastrar muitos EPIs de uma vez, por planilha, pelo número do CA.

{% hint style="info" %}
**Quem pode fazer:** Gestor ou Administrador, com a permissão de cadastrar novos itens de EPI.
{% endhint %}

## Antes de começar

* A planilha precisa ser .xlsx.

## Passo a passo

{% stepper %}
{% step %}
### Baixe o modelo

Clique em **Ações › Importar Itens por CA**. Clique em **Gerar Template** e preencha a planilha.

<figure><img src="../../.gitbook/assets/inventario-import-ca-01.png" alt="Janela Importar Itens por Certificado de Aprovação com Gerar Template e Importar Arquivo"><figcaption><p>Importar Itens por CA</p></figcaption></figure>
{% endstep %}

{% step %}
### Envie

Arraste o arquivo e clique em **Confirmar Importação**. Aparece "Processando importação" e depois **Importação concluída**: "Os itens foram cadastrados com sucesso no sistema".
{% endstep %}
{% endstepper %}

## Deu errado?

{% hint style="warning" %}
**"Apenas arquivos Excel (.xlsx) são aceitos"**: salve a planilha em .xlsx.
{% endhint %}

## Dúvidas comuns

<details>

<summary>Demora?</summary>

Arquivos grandes podem levar alguns minutos.

</details>

<details>

<summary>E os tipos de EPI NR-6?</summary>

A janela mostra **Atenção: Verificação NR-6**. Confira os **Tipos de EPIs NR-6** na planilha.

</details>
