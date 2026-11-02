---
description: Defina a reação e a eficácia padrão de um treinamento do catálogo.
icon: star-half-stroke
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

# Definir as avaliações de um treinamento

**Para que serve:** escolher o questionário de reação padrão e se o treinamento exige avaliação de eficácia.

{% hint style="info" %}
**Quem pode fazer:** Gestor ou Administrador, com a permissão de editar treinamentos.
{% endhint %}

## Antes de começar

* [Crie o questionário de reação](questionarios.md), se não for usar um padrão.

## Passo a passo

{% stepper %}
{% step %}
### Abra o treinamento

Clique em **Configurações › Tipos de Treinamentos**, abra o treinamento e vá à aba **Avaliações**.

<figure><img src="../.gitbook/assets/config-avaliacoes-01.png" alt="Aba Avaliações do treinamento com Avaliação de reação e Avaliação de eficácia"><figcaption><p>Aba Avaliações</p></figcaption></figure>
{% endstep %}

{% step %}
### Escolha a reação

Em **Questionário de reação**, escolha o questionário ou **Nenhum (a turma não gera reação)**.
{% endstep %}

{% step %}
### Escolha a eficácia

Em **Exige avaliação de eficácia**, escolha **Avaliar a eficácia de cada aprovado** ou **Não avaliar a eficácia**. Informe os **Dias depois do fim da turma**.
{% endstep %}

{% step %}
### Salve

Clique em **Salvar avaliações**. Aparece "Avaliações do treinamento salvas.".
{% endstep %}
{% endstepper %}

## Dúvidas comuns

<details>

<summary>O que acontece no dia da avaliação de eficácia?</summary>

Cada aprovado ganha uma avaliação agendada. Os gestores da unidade recebem um e-mail. O resultado é registrado em [Avaliar a eficácia](../turmas/avaliar-eficacia.md).

</details>

<details>

<summary>Posso usar outra reação numa turma?</summary>

Pode. Na turma, aba **Reação**. Veja [Ver a reação dos participantes](../turmas/reacao.md).

</details>
