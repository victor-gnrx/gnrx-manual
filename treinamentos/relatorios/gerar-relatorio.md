---
description: Gere relatórios de pendências, turmas, certificados e vencimentos.
icon: file-lines
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

# Gerar um relatório

**Para que serve:** listar quem está sem treinamento, as turmas realizadas, os certificados emitidos e os próximos vencimentos, e gerar o PDF.

{% hint style="info" %}
**Quem pode fazer:** Supervisor, Gestor ou Administrador, com a permissão de gerar relatórios de participação.
{% endhint %}

## Antes de começar

* Nada a preparar.

## Passo a passo

{% stepper %}
{% step %}
### Escolha o relatório

Clique em **Relatórios** e escolha:

* **Colaboradores sem Treinamento:** pendências de treinamentos obrigatórios, por unidade, grupo, cargo e setor.
* **Colaboradores por Treinamento:** quem ainda precisa fazer um treinamento específico.
* **Treinamentos Realizados:** por unidade e status.
* **Certificados Emitidos:** por unidade, grupo, setor e cargo.
* **Próximos Vencimentos:** certificados que vencem em 30, 60, 90 ou 180 dias.

<figure><img src="../.gitbook/assets/relatorios-01.png" alt="Tela Relatórios com a lista de relatórios disponíveis"><figcaption><p>Relatórios</p></figcaption></figure>
{% endstep %}

{% step %}
### Filtre

Escolha os filtros (unidade, GHE, cargo, setor, status). **Limpar filtros** volta ao início.
{% endstep %}

{% step %}
### Gere o PDF

Clique em **Gerar PDF** (ou **Exportar PDF**). Aparece "PDF gerado com sucesso!".
{% endstep %}
{% endstepper %}

## Deu errado?

{% hint style="warning" %}
**"Erro ao gerar PDF"**: tente novamente.
{% endhint %}

## Dúvidas comuns

<details>

<summary>Preciso de um relatório que não existe.</summary>

Clique em **Solicitar relatório**, descreva o que precisa e clique em **Enviar solicitação**.

</details>

<details>

<summary>Apareceu "Todos os colaboradores estão em conformidade."</summary>

Ninguém está com pendência nos filtros escolhidos.

</details>
