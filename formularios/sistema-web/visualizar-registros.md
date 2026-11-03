---
description: "Lance, edite e exclua registros; conclua ou reabra o formulário."
icon: table
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

# Lançar os registros de um formulário

**Para que serve:** preencher o formulário: cada registro é uma linha (ex.: um extintor inspecionado).

{% hint style="info" %}
**Quem pode fazer:** todas as roles. Lançar exige a permissão de preencher registros; concluir e reabrir, a de editar formulários.
{% endhint %}

## Antes de começar

* O formulário precisa estar **Em Andamento**.

## Passo a passo

{% stepper %}
{% step %}
### Lance o registro

Abra o formulário e clique em **Novo Registro**. Preencha os campos e clique em **Salvar**. Aparece "Registro criado com sucesso!".

<figure><img src="../.gitbook/assets/form-registros-01.png" alt="Formulário aberto com os registros, Novo Registro, Concluir Formulário, Exportar XLSX e Relatórios"><figcaption><p>Registros do formulário</p></figcaption></figure>
{% endstep %}

{% step %}
### Edite ou exclua

Na linha, em **Opções**, use **Editar** (aparece "Registro atualizado com sucesso!") ou **Excluir** (não pode ser desfeito).
{% endstep %}

{% step %}
### Conclua

Clique em **Concluir Formulário** e confirme em **Sim, concluir formulário**. Depois de concluído, não é possível fazer alterações.
{% endstep %}
{% endstepper %}

## Deu errado?

| Mensagem na tela | O que fazer |
| --- | --- |
| "Valor não é um número válido" | Digite só números. |
| "Use o formato YYYY-MM-DD" / "Use o formato HH:MM" | Ajuste a data ou a hora. |
| "Corrija os dados obrigatórios primeiro" | Preencha os dados obrigatórios antes de concluir. |

## Dúvidas comuns

<details>

<summary>Tem registros em rascunho e não consigo concluir.</summary>

Use **Excluir rascunhos e concluir**. Os rascunhos são excluídos.

</details>

<details>

<summary>Preciso mexer num formulário concluído.</summary>

Clique em **Reabrir Formulário**. Ele volta para **Em andamento**.

</details>
