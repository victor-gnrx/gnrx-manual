---
description: Defina o estoque mínimo e o crítico de um item por centro de estoque.
icon: gauge-low
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

# Definir o estoque mínimo

**Para que serve:** receber alerta quando o estoque de um item fica baixo, em cada centro de estoque.

{% hint style="info" %}
**Quem pode fazer:** Administrador, com a permissão de gerenciar o estoque de EPIs.
{% endhint %}

## Antes de começar

* Escolha o centro de estoque.

## Passo a passo

{% stepper %}
{% step %}
### Abra o estoque mínimo

Abra o item e use **Configurar Estoque Mínimo**.

<figure><img src="../../.gitbook/assets/inventario-minimo-01.png" alt="Janela Configurar Estoque Mínimo com Quantidade Mínima, Quantidade Crítica e Variantes"><figcaption><p>Configurar Estoque Mínimo</p></figcaption></figure>
{% endstep %}

{% step %}
### Preencha

Informe a **Quantidade Mínima** (aciona alerta de estoque baixo) e, se quiser, a **Quantidade Crítica** (alerta crítico). Se o item tem variantes, escolha uma variação de cada tipo. Salve. Aparece "Configuração criada com sucesso!".
{% endstep %}
{% endstepper %}

## Deu errado?

| Mensagem na tela | O que fazer |
| --- | --- |
| "Quantidade crítica deve ser menor que a quantidade mínima" | Ajuste os valores. |
| "Selecione um centro de estoque antes." | Escolha o centro. |
| "Esta combinação de variações já existe" | Edite a configuração existente. |

## Dúvidas comuns

<details>

<summary>Vários itens equivalentes somam o estoque?</summary>

Use um [grupo de estoque](../../configuracoes-iniciais/grupos-estoque/criar-grupo-estoque.md).

</details>

<details>

<summary>Quem recebe o alerta?</summary>

Os e-mails da unidade com **Alertas de Estoque Mínimo** marcado.

</details>
