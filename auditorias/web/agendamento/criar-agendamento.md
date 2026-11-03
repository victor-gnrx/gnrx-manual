---
description: "Faça o GNRx criar auditorias sozinho, na frequência que você definir."
icon: calendar-plus
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

# Agendar auditorias automáticas

**Para que serve:** fazer o GNRx criar as auditorias sozinho, na frequência certa, e avisar quem executa. Ex.: inspeção de extintores todo dia 5.

{% hint style="info" %}
**Quem pode fazer:** todas as roles.
{% endhint %}

## Antes de começar

* Tenha um modelo [NR](../modelo-nr.md) ou [customizado](../modelo-customizado.md) disponível.
* Tenha os usuários que vão executar cadastrados. Veja [Criar um usuário](../estrutura/usuarios/criar-usuario.md).

## Passo a passo

{% stepper %}
{% step %}
### Abra o novo agendamento

Clique em **Agendamento de Auditorias** e em **Novo Agendamento**.

<figure><img src="../../.gitbook/assets/aud-agendamento-01.png" alt="Tela Novo Agendamento com Informações Básicas, Modelo de Checklist, Período de Vigência e Recorrência"><figcaption><p>Novo Agendamento</p></figcaption></figure>
{% endstep %}

{% step %}
### Preencha o básico

Informe o **Código**, o **Nome** e, se quiser, a **Descrição**. Escolha o **Modelo** e, se quiser, a **Unidade** e o **Setor**.
{% endstep %}

{% step %}
### Defina quando

Em **Período de Vigência**, informe a **Data Início** e, se quiser, a **Data Fim**. Em **Recorrência**, escolha a **Frequência** (Diária, Semanal, Mensal ou Anual) e o **Intervalo**. Confira o **Resumo da Recorrência**.
{% endstep %}

{% step %}
### Escolha as pessoas

Em **Executores**, adicione pelo menos um usuário. Arraste para mudar a ordem de execução. Se quiser, adicione **Gestores** para receber e-mail antes da execução ou após a conclusão.
{% endstep %}

{% step %}
### Crie

Em **Configurações de Notificação**, marque **Notificar Executores** e os **Dias de Antecedência**, se quiser. Clique em **Criar Agendamento**.
{% endstep %}
{% endstepper %}

## Deu errado?

{% hint style="warning" %}
**"Corrija os seguintes erros:"**: corrija cada campo da lista e clique em **Criar Agendamento** de novo.
{% endhint %}

## Dúvidas comuns

<details>

<summary>Semanal ou mensal sem escolher o dia?</summary>

O GNRx usa o dia da **Data Início**.

</details>

<details>

<summary>Como altero ou paro o agendamento?</summary>

Veja [Editar ou inativar um agendamento](editar-agendamento.md).

</details>
