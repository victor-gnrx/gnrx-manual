---
description: "Abra uma auditoria a partir de um modelo."
icon: clipboard-check
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

# Criar uma auditoria

**Para que serve:** abrir uma auditoria nova, numa unidade e num setor, a partir de um modelo. Ex.: inspeção de extintores do almoxarifado.

{% hint style="info" %}
**Quem pode fazer:** todas as roles, com a permissão de criar auditorias.
{% endhint %}

## Antes de começar

* Tenha um modelo [NR](modelo-nr.md) ou [customizado](modelo-customizado.md) disponível.
* Tenha a [unidade](estrutura/unidades/criar-unidade.md) vinculada ao seu usuário, com o [setor](estrutura/setores/criar-setor.md) associado a ela.

## Passo a passo

{% stepper %}
{% step %}
### Abra a nova auditoria

Clique em **Auditorias** e em **Nova auditoria**.

<figure><img src="../.gitbook/assets/aud-nova-01.png" alt="Janela Criar Nova Auditoria com Unidade, Setor, Tipo de Modelo, Modelo e Descrição"><figcaption><p>Criar Nova Auditoria</p></figcaption></figure>
{% endstep %}

{% step %}
### Escolha onde e o quê

Escolha a **Unidade**, o **Setor**, o **Tipo de Modelo** (Modelo NR ou Modelo Customizado) e o **Modelo**.
{% endstep %}

{% step %}
### Preencha o cabeçalho

Se o modelo tiver **Cabeçalho**, preencha os campos. Os marcados como **Obrigatório** não podem ficar vazios. Se quiser, escreva a **Descrição**.
{% endstep %}

{% step %}
### Crie

Clique em **Criar Auditoria**. O GNRx abre a página da auditoria.
{% endstep %}
{% endstepper %}

## Deu errado?

| Mensagem na tela | O que fazer |
| --- | --- |
| "Unidade é obrigatória" | Escolha a unidade. |
| "Setor é obrigatório" | Escolha o setor. |
| "Modelo é obrigatório" | Escolha o modelo. |
| "Descrição não pode exceder 255 caracteres" | Encurte a descrição. |
| "Ocorreu um erro ao carregar os dados" | Feche a janela e abra de novo. |

## Dúvidas comuns

<details>

<summary>E agora?</summary>

Preencha a auditoria. Veja [Preencher uma auditoria](preencher-auditoria.md).

</details>

<details>

<summary>Não acho a unidade ou o setor?</summary>

A unidade precisa estar vinculada ao seu usuário e o setor precisa estar associado a ela. Fale com o administrador.

</details>

<details>

<summary>Não acho o modelo?</summary>

O modelo customizado precisa estar **Disponível**. Veja [Disponibilizar, revisar ou inativar um modelo](modelos/disponibilizar-modelo.md).

</details>

<details>

<summary>Pelo celular?</summary>

Também dá. Veja o [aplicativo](../aplicativo/nova-auditoria.md).

</details>
