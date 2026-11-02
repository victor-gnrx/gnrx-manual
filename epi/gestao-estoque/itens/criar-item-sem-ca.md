---
description: Cadastre um produto simples, sem CA.
icon: box
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

# Cadastrar um produto sem CA

**Para que serve:** cadastrar um item simples, sem CA (uniforme, ferramenta, máquina).

{% hint style="info" %}
**Quem pode fazer:** Gestor ou Administrador, com a permissão de cadastrar novos itens de EPI.
{% endhint %}

## Antes de começar

* O tipo de produto precisa existir em [Tipos de produtos](../../configuracoes-gerais/epis/adicionar-epi-catalogo.md).

## Passo a passo

{% stepper %}
{% step %}
### Clique em Novo Item

Clique em **Inventário › Gerenciar Inventário** e depois em **Novo Item**. Escolha **Produto** (item simples, sem CA).

<figure><img src="../../.gitbook/assets/inventario-criar-produto-01.png" alt="Janela Criar Produto com Nome, Categoria, Tipos de Produto e Unidade de Medida"><figcaption><p>Criar Produto</p></figcaption></figure>
{% endstep %}

{% step %}
### Preencha

Informe o nome, a **Categoria**, os **Tipos de Produto** e a **Unidade de Medida** (**Inteiro**, **Uma casa** ou **Três casas** decimais).
{% endstep %}

{% step %}
### Salve

Clique em **Salvar Produto**. Aparece "Produto criado com sucesso".
{% endstep %}
{% endstepper %}

## Deu errado?

| Mensagem na tela | O que fazer |
| --- | --- |
| "Categoria é obrigatória" | Escolha a categoria. |
| "Selecione pelo menos um tipo de produto" | Escolha o tipo. |

## Dúvidas comuns

<details>

<summary>Qual unidade de medida uso?</summary>

**Inteiro** para itens contados (1, 2, 5). Casas decimais para itens a granel (0,5 / 1,500).

</details>

<details>

<summary>Tenho muitos produtos.</summary>

Use **Ações › Importar Itens em Massa**.

</details>
