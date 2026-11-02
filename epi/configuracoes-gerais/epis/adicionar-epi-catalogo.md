---
description: Cadastre tipos de produto que não são EPI, como máquinas e uniformes.
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

# Criar um tipo de produto

**Para que serve:** cadastrar tipos de produto que não são EPI (máquinas, uniformes, equipamentos), organizados por categoria.

{% hint style="info" %}
**Quem pode fazer:** Gestor ou Administrador, com a permissão de cadastrar EPIs NR-6 customizados.
{% endhint %}

## Antes de começar

* Crie a categoria, se ela ainda não existe.

## Passo a passo

{% stepper %}
{% step %}
### Crie a categoria (se precisar)

Clique em **Configurações › Tipos de Produtos** e abra **Outros Tipos de Produtos**. Clique em **Nova Categoria**. Informe o nome (ex.: Máquinas, Uniformes, Ferramentas), a **Cor da Categoria** e o **Ícone da Categoria**. Clique em **Criar Categoria**. Aparece "Categoria criada com sucesso.".

<figure><img src="../../.gitbook/assets/produtos-outros-01.png" alt="Outros Tipos de Produtos com as categorias e a lista de tipos"><figcaption><p>Outros Tipos de Produtos</p></figcaption></figure>
{% endstep %}

{% step %}
### Crie o tipo de produto

Escolha a categoria e clique em **Novo Tipo de Produto**. Digite o nome e a descrição. Clique em **Criar Tipo de Produto**. Aparece "Produto criado com sucesso.".
{% endstep %}
{% endstepper %}

## Deu errado?

| Mensagem na tela | O que fazer |
| --- | --- |
| "Nome é obrigatório" | Preencha o nome. |
| "Categoria é obrigatória" | Escolha a categoria. |
| "Cor deve estar no formato #RRGGBB" | Escolha a cor pelo seletor. |

## Dúvidas comuns

<details>

<summary>Preciso trocar a categoria de um produto.</summary>

Use **Editar Categoria/Tipo**, escolha a nova categoria e salve. Aparece "Produto atualizado com sucesso.".

</details>

<details>

<summary>Como excluo uma categoria com produtos?</summary>

Em **Gerenciar Categorias**, use **Excluir categoria**. Se ela tiver produtos, **Mover produtos antes de excluir**: escolha a **Categoria de destino** e clique em **Mover e excluir categoria**.

</details>
