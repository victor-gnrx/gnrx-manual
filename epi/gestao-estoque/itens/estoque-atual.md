---
description: Veja o estoque de um item por centro de estoque, lote e unidade.
icon: warehouse
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

# Ver o estoque de um item

**Para que serve:** ver quanto há de um item em cada centro de estoque, por lote e por unidade.

{% hint style="info" %}
**Quem pode fazer:** Supervisor, Gestor ou Administrador, com a permissão de ver o estoque de EPIs.
{% endhint %}

## Antes de começar

* [Encontre o item](listar-itens.md).

## Passo a passo

{% stepper %}
{% step %}
### Abra o item

Na lista, abra o item. Veja as **Entradas de Estoque** e o estoque por centro.

<figure><img src="../../.gitbook/assets/inventario-estoque-01.png" alt="Detalhe do item com as entradas de estoque e o estoque por centro"><figcaption><p>Estoque do item</p></figcaption></figure>
{% endstep %}

{% step %}
### Veja as unidades

Abra uma entrada (lote) para ver cada unidade. Use **Pesquisar por número de série...**.
{% endstep %}
{% endstepper %}

## Dúvidas comuns

<details>

<summary>Como mudo o estado de uma unidade (ex.: enviar à lavanderia)?</summary>

Marque as unidades e escolha o **Novo estado**. Para lavanderia, use **Selecione a lavanderia**. Aparece "Estado alterado com sucesso!".

</details>

<details>

<summary>Como levo o estoque para um relatório?</summary>

Use **Ações › Relatórios** (estoque em PDF e movimentações).

</details>
