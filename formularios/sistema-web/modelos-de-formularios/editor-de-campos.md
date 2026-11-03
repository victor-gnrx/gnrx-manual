---
description: "Adicione os campos que a equipe vai preencher em cada registro."
icon: table-list
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

# Adicionar campos ao modelo

**Para que serve:** definir o que a equipe preenche em cada registro do formulário.

{% hint style="info" %}
**Quem pode fazer:** Gestor ou Administrador, com a permissão de criar ou editar modelos de formulário.
{% endhint %}

## Antes de começar

* Abra o modelo em **Novo Modelo** ou em **Editar**.

## Passo a passo

{% stepper %}
{% step %}
### Adicione o campo

Clique em **Adicionar Campo**. Informe o **Nome do Campo** e escolha o **Tipo** (veja [Escolher o tipo de campo](tipos-de-campos.md)).

<figure><img src="../../.gitbook/assets/form-campos-01.png" alt="Lista de campos com Nome do Campo, Tipo, Máscara/Opções/Padrão Obs. e Obrigatório"><figcaption><p>Campos do modelo</p></figcaption></figure>
{% endstep %}

{% step %}
### Complete

Em **Máscara/Opções/Padrão Obs.**, informe a máscara ou as opções, conforme o tipo. Para **Seleção Única** e **Seleção Múltipla**, use **Adicionar Opções**. Ligue **Obrigatório** se o campo não pode ficar vazio.
{% endstep %}

{% step %}
### Salve

Clique em **Salvar Modelo**.
{% endstep %}
{% endstepper %}

## Dúvidas comuns

<details>

<summary>A máscara aparece como "Não aplicável".</summary>

O tipo escolhido não aceita máscara.

</details>

<details>

<summary>Como agrupo os campos?</summary>

Veja [Organizar os campos em seções](secoes-e-organizacao.md).

</details>
