---
description: "Crie um modelo com nome, tipo, dados globais e campos."
icon: file-circle-plus
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

# Criar um modelo de formulário

**Para que serve:** definir um formulário que a equipe vai preencher várias vezes. Ex.: inspeção diária de extintores.

{% hint style="info" %}
**Quem pode fazer:** Gestor ou Administrador, com a permissão de criar modelos de formulário.
{% endhint %}

## Antes de começar

* Liste os campos que o formulário precisa ter.

## Passo a passo

{% stepper %}
{% step %}
### Abra o novo modelo

Clique em **Modelos de Formulário** e em **Novo Modelo**.

<figure><img src="../../.gitbook/assets/form-modelo-novo-01.png" alt="Janela Criar Novo Modelo de Formulário com nome, tipo, revisão, dados globais e campos"><figcaption><p>Criar Novo Modelo de Formulário</p></figcaption></figure>
{% endstep %}

{% step %}
### Preencha os dados

Informe o **Nome do Formulário** e o **Tipo do Formulário** (**Padrão**, **Checklist** ou **Auditoria**). Se quiser, escreva a **Descrição** e informe o **Nº Revisão** e a **Data da Revisão**. Deixe **Permitir novos registros** ligado para a equipe poder lançar registros.
{% endstep %}

{% step %}
### Adicione os dados globais (se quiser)

Dados globais são preenchidos uma vez por formulário (ex.: local, responsável). Clique em **Adicionar Dado Personalizado** e informe o nome, o tipo e se é obrigatório.
{% endstep %}

{% step %}
### Adicione os campos

Escolha **Campos Simples** ou **Campos com Seções** e use **Adicionar Campo**. Veja [Adicionar campos ao modelo](editor-de-campos.md).
{% endstep %}

{% step %}
### Salve

Clique em **Salvar Modelo**. Aparece "Modelo criado com sucesso".
{% endstep %}
{% endstepper %}

## Deu errado?

{% hint style="warning" %}
**"Data da revisão inválida. O campo será ignorado."**: o modelo é salvo sem a data. Corrija a data editando o modelo.
{% endhint %}

## Dúvidas comuns

<details>

<summary>Qual tipo escolher?</summary>

**Padrão** para formulários comuns, **Checklist** para listas de verificação e **Auditoria** para formulários de auditoria.

</details>

<details>

<summary>Posso mudar depois?</summary>

Pode. Veja [Editar, revisar ou inativar um modelo](versionamento.md).

</details>
