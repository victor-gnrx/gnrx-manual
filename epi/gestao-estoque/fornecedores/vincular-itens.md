---
description: Ligue os itens ao fornecedor, com preço, qualidade e prazo.
icon: link
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

# Vincular itens a um fornecedor

**Para que serve:** registrar o preço, a qualidade e o prazo de cada item no fornecedor, para comparar e comprar melhor.

{% hint style="info" %}
**Quem pode fazer:** Supervisor, Gestor ou Administrador, com a permissão de vincular e precificar itens do fornecedor.
{% endhint %}

## Antes de começar

* [Cadastre o fornecedor](cadastrar-fornecedor.md) e o item.

## Passo a passo

{% stepper %}
{% step %}
### Abra o fornecedor

Clique em **Inventário › Gerenciar Fornecedores** e abra o fornecedor. Clique em **Vincular item**.

<figure><img src="../../.gitbook/assets/fornecedores-vincular-01.png" alt="Janela Vincular item com Item, Preço, Qualidade, Prazo de entrega, SKU e vigência"><figcaption><p>Vincular item</p></figcaption></figure>
{% endstep %}

{% step %}
### Preencha

Escolha o **Item** e informe o **Preço**, a **Qualidade (0–100)**, o **Prazo de entrega (dias)** e o **SKU do fornecedor**. Informe o **Início da vigência** (em branco = hoje) e, se quiser, o **Fim da vigência**. Clique em **Vincular**. Aparece "Item vinculado ao fornecedor.".
{% endstep %}
{% endstepper %}

## Deu errado?

| Mensagem na tela | O que fazer |
| --- | --- |
| "Selecione um item" | Escolha o item. |
| "Máximo 100" | A qualidade vai de 0 a 100. |
| "O fim da vigência não pode ser antes do início" | Confira as datas. |

## Dúvidas comuns

<details>

<summary>Como tiro um item do fornecedor?</summary>

Use **Remover vínculo**. O preço deixa de ser considerado nos comparativos.

</details>

<details>

<summary>O preço mudou.</summary>

Edite o vínculo e salve. Aparece "Vínculo atualizado.".

</details>
