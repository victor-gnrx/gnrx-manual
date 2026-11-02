---
description: Crie uma variante (tamanho, cor, modelo) num item.
icon: plus
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

# Criar uma variante

**Para que serve:** criar uma variante num item (ex.: Tamanho, com P, M e G), para separar o estoque.

{% hint style="info" %}
**Quem pode fazer:** Gestor ou Administrador, com a permissão de editar itens de EPI.
{% endhint %}

## Antes de começar

* Abra o item no inventário. Crie as variantes antes de dar entrada no estoque.

## Passo a passo

{% stepper %}
{% step %}
### Abra a variante

No item, clique em **Nova Variante**. Abre **Adicionar Nova Variante**.

<figure><img src="../../.gitbook/assets/inventario-variante-01.png" alt="Janela Adicionar Nova Variante com Nome da Variante, Variante Obrigatória e Valores da Variante"><figcaption><p>Adicionar Nova Variante</p></figcaption></figure>
{% endstep %}

{% step %}
### Preencha

Dê o **Nome da Variante** (ex.: Tamanho, Cor, Modelo). Se toda entrada precisa dela, ligue **Variante Obrigatória**. Em **Valores da Variante**, digite cada valor e clique em **Adicionar**.
{% endstep %}

{% step %}
### Crie

Clique em **Criar Variante**. Aparece "Variante criada com sucesso!".
{% endstep %}
{% endstepper %}

## Deu errado?

| Mensagem na tela | O que fazer |
| --- | --- |
| "Nome da variante é obrigatório" | Dê o nome. |
| "Adicione pelo menos um valor" | Adicione um valor. |
| "Existem valores duplicados" | Tire o repetido. |

## Dúvidas comuns

<details>

<summary>Esqueci um valor.</summary>

Veja [Adicionar valores a uma variante](adicionar-valores-variante.md).

</details>

<details>

<summary>Como uso na entrada?</summary>

Na [entrada de estoque](../itens/adicionar-lote.md), distribua a quantidade pelas combinações.

</details>
