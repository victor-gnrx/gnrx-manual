---
description: Diga quem precisa entregar cada documento, e em quais casos.
icon: table-cells
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

# Montar a matriz de exigência

**Para que serve:** dizer quem precisa entregar cada documento e em quais casos. Ex.: ASO de todo funcionário próprio.

{% hint style="info" %}
**Quem pode fazer:** Gestor ou Administrador, com a permissão de editar a matriz de exigência. Todas as roles podem ver.
{% endhint %}

## Antes de começar

* Cadastre os [tipos de documento](tipos-de-documento.md).

## Passo a passo

{% stepper %}
{% step %}
### Comece a exigência

Clique em **Configurações › Matriz de exigência** e depois em **Nova exigência**. Em **Qual documento será exigido?**, busque o documento.

<figure><img src="../.gitbook/assets/docs-matriz-01.png" alt="Assistente Nova exigência com Qual documento, De quem e Em quais casos"><figcaption><p>Nova exigência</p></figcaption></figure>
{% endstep %}

{% step %}
### De quem

Em **De quem ele é exigido?**, escolha: a sua própria empresa, cada unidade, a empresa terceira contratada, cada pessoa da equipe terceirizada ou cada colaborador da sua empresa.
{% endstep %}

{% step %}
### Em quais casos

Escolha **Todos os casos** ou uma condição: uma unidade, um GHE exposto a um risco, um cargo, uma contratada ou um tipo de serviço.
{% endstep %}

{% step %}
### Como cobrar

Escolha se é obrigatório (se faltar, o titular fica irregular) ou não (se faltar, fica pendente, nunca irregular). Se quiser, informe o **Prazo para entregar após a admissão**. Clique em **Criar exigência**. Aparece "Exigência criada.".
{% endstep %}
{% endstepper %}

## Dúvidas comuns

<details>

<summary>Posso copiar a matriz para outras unidades?</summary>

Pode. Use **Copiar a matriz da unidade** e escolha as unidades.

</details>

<details>

<summary>Como deixo de exigir um documento?</summary>

Inative a regra. Ela deixa de ser exigida, e a situação dos titulares é recalculada.

</details>
