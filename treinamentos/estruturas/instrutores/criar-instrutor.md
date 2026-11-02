---
description: Cadastre um instrutor interno ou externo.
icon: user-plus
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

# Criar um instrutor

**Para que serve:** cadastrar quem vai ministrar os treinamentos.

{% hint style="info" %}
**Quem pode fazer:** Gestor ou Administrador, com a permissão de cadastrar instrutores.
{% endhint %}

## Antes de começar

* Instrutor interno: ele precisa estar cadastrado como [colaborador](../colaboradores/criar-colaborador.md).
* Instrutor externo: tenha o CPF dele.

## Passo a passo

{% stepper %}
{% step %}
### Clique em Novo instrutor

Clique em **Estruturas › Instrutores** e depois em **Novo instrutor**. Abre **Criar novo instrutor**.

<figure><img src="../../.gitbook/assets/instrutores-criar-01.png" alt="Janela Criar novo instrutor com o Tipo de instrutor e os dados pessoais e profissionais"><figcaption><p>Criar novo instrutor</p></figcaption></figure>
{% endstep %}

{% step %}
### Escolha o tipo

Em **Tipo de instrutor**, escolha:

* **Interno (colaborador):** clique em **Buscar colaborador**, digite o nome ou o CPF e escolha a pessoa.
* **Externo:** preencha o nome completo e o CPF.
{% endstep %}

{% step %}
### Complete os dados

Se quiser, preencha **Telefone**, **E-mail**, **Registro Profissional** (ex.: CREA 123456), **Órgão de Registro** (ex.: CREA-MG), **Formação Acadêmica** e **Observações**.
{% endstep %}

{% step %}
### Crie

Clique em **Criar instrutor**. Aparece "Instrutor criado com sucesso".
{% endstep %}
{% endstepper %}

## Deu errado?

| Mensagem na tela | O que fazer |
| --- | --- |
| "Instrutor interno deve estar vinculado a um funcionário" | Clique em **Buscar colaborador** e escolha a pessoa. |
| "Instrutor externo deve ter CPF informado" | Preencha o CPF. |
| "Nome deve ter no mínimo 3 caracteres" | Escreva o nome completo. |
| "CPF inválido" | Confira o CPF. |

## Dúvidas comuns

<details>

<summary>Qual a diferença entre interno e externo?</summary>

O interno é um colaborador da empresa. O externo é alguém de fora, cadastrado só com os dados dele.

</details>

<details>

<summary>Onde vejo o que o instrutor já ministrou?</summary>

Na lista, clique em **Ver Detalhes**. A aba **Treinamentos** mostra os **Treinamentos Ministrados**.

</details>
