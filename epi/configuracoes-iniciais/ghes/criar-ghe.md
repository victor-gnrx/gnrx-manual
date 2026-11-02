---
description: Cadastre um grupo de colaboradores com os mesmos riscos.
icon: plus
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

# Criar um GHE

**Para que serve:** cadastrar um grupo de colaboradores expostos aos mesmos riscos, dentro de uma unidade.

{% hint style="info" %}
**Quem pode fazer:** Gestor ou Administrador, com a permissão de cadastrar GHEs.
{% endhint %}

## Antes de começar

* Cadastre a [unidade](../unidades/criar-unidade.md).

## Passo a passo

{% stepper %}
{% step %}
### Clique em Novo Grupo

Clique em **Estruturas**, abra os GHEs (no módulo Gestão de EPIs, **Estruturas › GHEs — Grupos de EPIs**) e clique em **Novo Grupo**. Abre **Criar Novo Grupo**.

<figure><img src="../../.gitbook/assets/ghe-criar-01.png" alt="Janela Criar Novo Grupo com Nome, Unidade, Descrição, Medidas de controle e a opção Copiar configurações de outro grupo"><figcaption><p>Janela Criar Novo Grupo</p></figcaption></figure>
{% endstep %}

{% step %}
### Preencha os dados

Preencha o **Nome** e escolha a **Unidade**. Se quiser, preencha a descrição ("Descreva o Grupo...") e as medidas de controle.
{% endstep %}

{% step %}
### Copie de outro grupo (opcional)

Para aproveitar a configuração de um GHE parecido, use **Copiar configurações de outro grupo**. Se quiser, filtre por unidade e escolha o grupo.
{% endstep %}

{% step %}
### Salve

Clique em **Salvar**. Aparece "Grupo criado com sucesso" (ou "Grupo criado com sucesso e configurações copiadas").
{% endstep %}
{% endstepper %}

No módulo Gestão de EPIs, o próximo passo é vincular os riscos, na aba **Riscos / EPIs** do GHE.

## Deu errado?

| Mensagem na tela | O que fazer |
| --- | --- |
| "Obrigatório" | Preencha o nome e escolha a unidade. |
| "Nome muito longo", "Descrição muito longa" ou "Medidas de controle muito longo" | Encurte o texto. |

## Dúvidas comuns

<details>

<summary>Um GHE vale para várias unidades?</summary>

Não. Cada GHE fica numa unidade. Para outra unidade, crie outro GHE e copie a configuração.

</details>

<details>

<summary>Preciso copiar de outro grupo?</summary>

Não. A cópia é opcional. Sem ela, você configura o GHE do zero.

</details>
