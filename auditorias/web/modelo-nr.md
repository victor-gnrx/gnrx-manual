---
description: "Monte um checklist com itens da biblioteca de NRs."
icon: scale-balanced
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

# Criar um modelo NR

**Para que serve:** montar um checklist com itens tirados das Normas Regulamentadoras. Ex.: inspeção de máquinas pela NR-12.

{% hint style="info" %}
**Quem pode fazer:** Gestor ou Administrador, com as permissões de criar e de editar modelos.
{% endhint %}

## Passo a passo

{% stepper %}
{% step %}
### Abra o novo modelo

Clique em **Modelos NRs** e em **Novo Modelo NR**.

<figure><img src="../.gitbook/assets/aud-modelo-nr-01.png" alt="Janela Criar Novo Modelo NR com Código, Nome e Descrição"><figcaption><p>Criar Novo Modelo NR</p></figcaption></figure>
{% endstep %}

{% step %}
### Preencha e crie

Informe o **Código**, o **Nome** e, se quiser, a **Descrição**. Clique em **Criar Modelo**. Aparece "Modelo NR criado com sucesso."
{% endstep %}

{% step %}
### Crie uma seção

Clique no nome do modelo para abri-lo. Clique em **Nova Seção**, informe **Nome**, **Código**, **Ordem** e, se quiser, a **Descrição**, e clique em **Criar Seção**.
{% endstep %}

{% step %}
### Inclua os itens da NR

Clique em **Selecionar Items NR da seção**. Navegue pelas NRs e marque os itens. Clique em **Salvar**, revise e clique em **Confirmar**.

<figure><img src="../.gitbook/assets/aud-modelo-nr-02.png" alt="Janela de seleção com a lista de Normas Regulamentadoras e os itens marcados"><figcaption><p>Selecionar os itens da NR</p></figcaption></figure>
{% endstep %}
{% endstepper %}

## Deu errado?

{% hint style="warning" %}
**"Código é obrigatório"**: informe o código.
{% endhint %}

{% hint style="warning" %}
**"Nome é obrigatório"**: informe o nome.
{% endhint %}

## Dúvidas comuns

<details>

<summary>Como tiro um item ou uma seção?</summary>

Use o ícone de lixeira do item ou da seção e confirme em **Confirmar Desvinculação**. O histórico das auditorias já feitas é mantido.

</details>

<details>

<summary>Como mudo o nome ou o código?</summary>

Em **Modelos NRs**, abra o menu da linha e clique em **Editar**.

</details>

<details>

<summary>Dá para levar o modelo para o Excel?</summary>

Sim. Dentro do modelo, clique em **Exportar Excel** e escolha **Planilha de Preenchimento** (para preencher fora do sistema) ou **Estrutura Detalhada** (seções, itens e alíneas).

</details>

<details>

<summary>Como inativo o modelo?</summary>

No menu da linha, clique em **Inativar**. Pede a permissão de excluir modelos.

</details>
