---
description: "Altere os dados de um agendamento ou pare as auditorias automáticas."
icon: calendar-xmark
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

# Editar ou inativar um agendamento

**Para que serve:** mudar o nome ou os avisos de um agendamento, ou parar de criar as auditorias automáticas.

{% hint style="info" %}
**Quem pode fazer:** todas as roles.
{% endhint %}

## Antes de começar

* Tenha um [agendamento](criar-agendamento.md) criado.

## Passo a passo

{% stepper %}
{% step %}
### Abra o menu

Clique em **Agendamento de Auditorias** e abra o menu da linha.

<figure><img src="../../.gitbook/assets/aud-agendamento-02.png" alt="Lista de agendamentos com Frequência, Próxima Execução e o menu da linha aberto com Editar e Inativar"><figcaption><p>Agendamentos de Auditoria</p></figcaption></figure>
{% endstep %}

{% step %}
### Para editar

Clique em **Editar**. Altere o **Nome**, a **Descrição** ou os avisos e clique em **Salvar Alterações**.
{% endstep %}

{% step %}
### Para inativar

Clique em **Inativar**, leia o que vai acontecer e clique em **Inativar Agendamento**. Aparece "Agendamento inativado com sucesso".
{% endstep %}
{% endstepper %}

## Dúvidas comuns

<details>

<summary>O que acontece ao inativar?</summary>

As execuções futuras são canceladas, os avisos param e nenhuma auditoria nova é criada. As auditorias já criadas continuam.

</details>

<details>

<summary>Como mudo o modelo ou a frequência?</summary>

Não dá na edição. Inative e crie um agendamento novo.

</details>
