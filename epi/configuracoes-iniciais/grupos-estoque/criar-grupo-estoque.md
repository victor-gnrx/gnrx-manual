---
description: Junte itens e CAs num grupo para somar o estoque e definir o mínimo.
icon: layer-group
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

# Criar um grupo de estoque

**Para que serve:** juntar itens ou CAs equivalentes (ex.: Máscara PFF2 de várias marcas) para somar o estoque e definir o estoque mínimo do grupo.

{% hint style="info" %}
**Quem pode fazer:** Gestor ou Administrador, com a permissão de cadastrar grupos de estoque. Todas as roles podem ver.
{% endhint %}

## Antes de começar

* Os itens precisam estar no catálogo, com a mesma unidade de medida.

## Passo a passo

{% stepper %}
{% step %}
### Crie o grupo

Clique em **Estruturas › Grupos de Estoque** e depois em **Novo Grupo**. Em **Criar Grupo de Estoque**, dê um nome (ex.: Máscara PFF2) e, se quiser, a descrição. Salve. Aparece "Grupo de estoque criado com sucesso".

<figure><img src="../../.gitbook/assets/grupos-estoque-01.png" alt="Detalhe do grupo de estoque com os itens e o estoque mínimo"><figcaption><p>Grupo de estoque</p></figcaption></figure>
{% endstep %}

{% step %}
### Adicione os itens

Abra o grupo e adicione os itens. Use **Buscar itens por nome ou CA...**.
{% endstep %}

{% step %}
### Configure o estoque mínimo

Use **Configurar Estoque Mínimo**. Escolha o centro de estoque e informe o mínimo e o crítico. Salve. Aparece "Configuração criada com sucesso!".
{% endstep %}
{% endstepper %}

## Deu errado?

| Mensagem na tela | O que fazer |
| --- | --- |
| "Todos os itens do catálogo já pertencem a este grupo ou usam uma unidade de medida diferente da já usada nele." | Use itens com a mesma unidade de medida. |
| "A crítica deve ser menor que a mínima" | Ajuste os valores. |
| "Adicione itens ao grupo antes de configurar o estoque mínimo" | Adicione os itens primeiro. |

## Dúvidas comuns

<details>

<summary>Como tiro um item do grupo?</summary>

Use **Remover do grupo**. Aparece "Item removido do grupo com sucesso".

</details>

<details>

<summary>Inativei o grupo. E os itens?</summary>

Os itens continuam existindo normalmente, só deixam de pertencer ao grupo.

</details>
