---
description: Cadastre as instituições que emitem certificados.
icon: building-columns
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

# Cadastrar uma instituição certificadora

**Para que serve:** cadastrar quem emite certificados (ex.: SENAI), para usar ao anexar certificados.

{% hint style="info" %}
**Quem pode fazer:** Gestor ou Administrador, com a permissão de criar instituições certificadoras. Para inativar: Administrador.
{% endhint %}

## Antes de começar

* Tenha o nome, a sigla e o CNPJ da instituição.

## Passo a passo

{% stepper %}
{% step %}
### Abra as instituições

Clique em **Configurações › Instituições Certificadoras**. Use **Pesquisar por nome, sigla ou CNPJ...**.

<figure><img src="../.gitbook/assets/config-instituicoes-01.png" alt="Tela Instituições Certificadoras com a busca, o filtro de tipo e os cartões das instituições"><figcaption><p>Instituições Certificadoras</p></figcaption></figure>
{% endstep %}

{% step %}
### Clique em Nova Instituição

Clique em **Nova Instituição**. Preencha o nome (ex.: SENAI - Serviço Nacional de Aprendizagem Industrial), a **Sigla**, o **Tipo de Instituição**, o **CNPJ** (só números), o **Website** e as **Observações**.
{% endstep %}

{% step %}
### Salve

Salve. Aparece "Instituição certificadora criada com sucesso!".
{% endstep %}
{% endstepper %}

## Deu errado?

| Mensagem na tela | O que fazer |
| --- | --- |
| "CNPJ deve conter 14 dígitos numéricos" | Digite só os 14 números. |
| "URL inválida" | Confira o site (ex.: https://exemplo.com.br). |

## Dúvidas comuns

<details>

<summary>O tipo de instituição que preciso não existe.</summary>

Clique em **Ver Tipos de Instituição** e depois em **Novo Tipo**.

</details>

<details>

<summary>Como tiro uma instituição da lista?</summary>

No cartão, inative e confirme em **Inativar Instituição**. "A instituição não aparecerá mais na lista."

</details>
