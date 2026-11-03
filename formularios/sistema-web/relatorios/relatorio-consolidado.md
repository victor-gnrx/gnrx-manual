---
description: "Gere um PDF com vários formulários de um modelo e unidade."
icon: copy
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

# Emitir vários formulários em um PDF

**Para que serve:** gerar um PDF único com os formulários de um modelo, numa unidade e num período.

{% hint style="info" %}
**Quem pode fazer:** Gestor ou Administrador, com a permissão de gerar relatórios de formulários em PDF.
{% endhint %}

## Antes de começar

* Em **Meus Formulários**, filtre o **Modelo**, a **Unidade** e o período.

## Passo a passo

{% stepper %}
{% step %}
### Abra a emissão

Clique em **Emissão em Massa**.

<figure><img src="../../.gitbook/assets/form-massa-01.png" alt="Janela Exportar Formulário com as Opções de Exportação e o botão Gerar PDF"><figcaption><p>Exportar Formulário</p></figcaption></figure>
{% endstep %}

{% step %}
### Gere

Em **Opções de Exportação**, marque o que quer: **Incluir "Criado por"**, **Incluir "Criado em"**, **Quebra de página entre formulários** e **Incluir índice**. Clique em **Gerar PDF**. Aparece "Relatório gerado com sucesso".
{% endstep %}
{% endstepper %}

## Deu errado?

| Mensagem na tela | O que fazer |
| --- | --- |
| **Emissão em Massa** apagado | Filtre o **Modelo** e a **Unidade**. |
| "Selecione uma data de início e fim" | Escolha o período. |

## Dúvidas comuns

<details>

<summary>Só um formulário?</summary>

Veja [Exportar um formulário](exportacao-de-dados.md).

</details>

<details>

<summary>Posso juntar modelos diferentes?</summary>

Não. A emissão é de um modelo por vez.

</details>
