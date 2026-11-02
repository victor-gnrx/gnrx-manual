---
description: No EPI, coloque o colaborador num GHE pela tela dele.
icon: people-group
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

# Vincular um GHE a um colaborador

**Para que serve:** colocar o colaborador num GHE pela tela dele, no módulo Gestão de EPIs.

{% hint style="info" %}
**Quem pode fazer:** Supervisor, Gestor ou Administrador, com a permissão de editar colaboradores.
{% endhint %}

## Antes de começar

* [Vincule a unidade](vincular-unidades.md) ao colaborador.
* O [GHE](../ghes/criar-ghe.md) precisa existir nessa unidade.

## Passo a passo

{% stepper %}
{% step %}
### Abra o colaborador

Clique em **Estruturas › Colaboradores**. Na coluna **Ações**, abra o menu e clique em **Visualizar**.
{% endstep %}

{% step %}
### Associe o GHE

Na unidade, clique em **Ghe**. Na janela **Associar ghe**, escolha o GHE ("Selecione um ghe...") e clique em **Associar**. Aparece "Ghe associado com sucesso".

<figure><img src="../../.gitbook/assets/colaboradores-ghe-01.png" alt="Unidade do colaborador com o botão Ghe e a janela Associar ghe aberta"><figcaption><p>Associar ghe</p></figcaption></figure>
{% endstep %}
{% endstepper %}

{% hint style="info" %}
**Para remover:** clique no ícone de lixeira do GHE e confirme em **Remover Grupo**. Aparece "Grupo removido com sucesso".
{% endhint %}

## Dúvidas comuns

<details>

<summary>Apareceu "Nenhum ghe disponível...".</summary>

A unidade não tem GHE ativo. [Crie um GHE](../ghes/criar-ghe.md) nela.

</details>

<details>

<summary>Dá para adicionar várias pessoas de uma vez?</summary>

Dá, pela tela do GHE. Veja [Adicionar colaboradores a um GHE](../ghes/colaboradores-do-ghe.md).

</details>
