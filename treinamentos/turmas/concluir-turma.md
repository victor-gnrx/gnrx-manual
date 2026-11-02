---
description: Encerre a turma e defina quem foi aprovado.
icon: flag-checkered
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

# Concluir a turma

**Para que serve:** encerrar a turma e definir quem foi aprovado.

{% hint style="info" %}
**Quem pode fazer:** Gestor ou Administrador, com a permissão de finalizar turmas.
{% endhint %}

## Antes de começar

* [Registre a presença](registrar-presenca.md) de todas as sessões.
* Cadastre a [assinatura do instrutor](../estruturas/instrutores/editar-instrutor.md). Ela sai no certificado.

## Passo a passo

{% stepper %}
{% step %}
### Clique em Concluir

Abra a turma e clique em **Concluir**. Abre **Concluir treinamento**: "Como os participantes serão avaliados?".

<figure><img src="../.gitbook/assets/turmas-concluir-01.png" alt="Janela Concluir treinamento com as opções Seleção manual, Percentual de presença e Presença + aprovação manual"><figcaption><p>Concluir treinamento</p></figcaption></figure>
{% endstep %}

{% step %}
### Escolha o critério

* **Seleção manual:** você escolhe quem foi aprovado. Use quando não há critério de presença.
* **Percentual de presença:** aprova automaticamente quem atingir o **Percentual mínimo de presença**.
* **Presença + aprovação manual:** precisa atingir o percentual **e** estar na lista de aprovados.
{% endstep %}

{% step %}
### Selecione e continue

Quando for o caso, marque os aprovados (**Selecionar elegíveis** marca quem atingiu a presença). Clique em **Continuar**. Aparece **Treinamento concluído!**, com os aprovados e os **Reprovados**.
{% endstep %}
{% endstepper %}

{% hint style="info" %}
Ao concluir, o certificado dos aprovados é gerado automaticamente. A validade sai do tipo de treinamento e o PDF fica pronto em alguns instantes. Ele já nasce válido, sem aprovação nem assinatura de ninguém, e pode ser conferido pelo QR Code ou pelo código público.
{% endhint %}

## Dúvidas comuns

<details>

<summary>Onde vejo os aprovados depois?</summary>

Na **Visão geral** da turma, em **Aprovados** e **Reprovados**, e na lista de **Participantes**.

</details>

<details>

<summary>O certificado saiu sem assinatura.</summary>

O PDF usa a assinatura cadastrada do instrutor e a do colaborador, se existirem. Sem elas, sai sem a imagem. Cadastre a [assinatura do instrutor](../estruturas/instrutores/editar-instrutor.md) antes de concluir.

</details>

<details>

<summary>Onde baixo o certificado?</summary>

Na lista de participantes, em **Baixar certificado**. Precisa da permissão de ver turmas.

</details>
