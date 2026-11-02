---
description: Cadastre os centros de estoque e ligue às unidades.
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

# Cadastrar um centro de estoque

**Para que serve:** cadastrar os lugares onde o estoque fica guardado (ex.: centro de distribuição) e ligar às unidades.

{% hint style="info" %}
**Quem pode fazer:** Gestor ou Administrador, com a permissão de criar centros de estoque. Todas as roles podem ver.
{% endhint %}

## Antes de começar

* Se você usa integração, tenha o código usado na coluna `centro_estoque_codigo`.

## Passo a passo

{% stepper %}
{% step %}
### Crie o centro de estoque

Clique em **Estruturas › Centros de Estoque** e depois em **Novo Centro de Estoque**. Em **Criar Centro de Estoque**, preencha o **Nome** (ex.: Centro de Distribuição SP), o endereço, o **Código de integração** (ex.: CENTRO-01) e a descrição. Clique em **Salvar**.

<figure><img src="../../.gitbook/assets/centro-estoque-criar-01.png" alt="Janela Criar Centro de Estoque com Nome, endereço e Código de integração"><figcaption><p>Criar Centro de Estoque</p></figcaption></figure>
{% endstep %}

{% step %}
### Associe as unidades

Abra o centro de estoque e associe as unidades atendidas por ele.
{% endstep %}
{% endstepper %}

## Deu errado?

| Mensagem na tela | O que fazer |
| --- | --- |
| "Nome é obrigatório" | Preencha o nome. |
| "Código muito longo" | Encurte o código. |

## Dúvidas comuns

<details>

<summary>Como tiro um centro de estoque?</summary>

Use **Inativar Centro de Estoque** e confirme. Aparece "Centro de estoque inativado com sucesso!".

</details>

<details>

<summary>Como corrijo os dados?</summary>

Use **Editar Centro de Estoque** e salve.

</details>
