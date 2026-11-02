---
description: Corrija os dados de um item do inventário.
icon: pen
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

# Editar um item

**Para que serve:** corrigir os dados de um item: nome, CA, validade, tempo de troca, fabricante.

{% hint style="info" %}
**Quem pode fazer:** Gestor ou Administrador, com a permissão de editar itens de EPI.
{% endhint %}

## Antes de começar

* [Encontre o item](listar-itens.md).

## Passo a passo

{% stepper %}
{% step %}
### Abra a edição

Na lista, clique no ícone de lápis, na coluna **Opções**. Abre a edição de EPI ou de Produto, conforme o item.

<figure><img src="../../.gitbook/assets/inventario-editar-01.png" alt="Janela de edição do item com os dados preenchidos"><figcaption><p>Editar item</p></figcaption></figure>
{% endstep %}

{% step %}
### Corrija e salve

Altere o que precisar e salve. Aparece "Item atualizado com sucesso!".
{% endstep %}
{% endstepper %}

## Deu errado?

{% hint style="warning" %}
**"Não é possível alterar com estoque cadastrado"**: o controle unitário não muda depois que o item tem estoque.
{% endhint %}

## Dúvidas comuns

<details>

<summary>O CA venceu. O que faço?</summary>

Atualize o número e a data de validade do CA.

</details>

<details>

<summary>Posso mudar o tempo de troca?</summary>

Pode. Ou marque **Não possui tempo de troca**.

</details>
