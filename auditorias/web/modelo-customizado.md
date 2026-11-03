---
description: "Monte o seu próprio checklist, com seções e itens de vários tipos."
icon: list-check
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

# Criar um modelo customizado

**Para que serve:** montar o checklist da sua empresa, com os itens e tipos de resposta que você precisa. Ex.: inspeção diária de empilhadeira com foto e assinatura.

{% hint style="info" %}
**Quem pode fazer:** Gestor ou Administrador, com as permissões de criar e de editar modelos.
{% endhint %}

## Passo a passo

{% stepper %}
{% step %}
### Abra o novo modelo

Clique em **Modelos Customizados** e em **Novo Modelo**.

<figure><img src="../.gitbook/assets/aud-modelo-custom-01.png" alt="Janela Criar Novo Checklist com Código, Nome, Descrição, Número da Revisão e Data da Revisão"><figcaption><p>Criar Novo Checklist</p></figcaption></figure>
{% endstep %}

{% step %}
### Preencha e crie

Informe o **Código**, o **Nome** e, se quiser, a **Descrição**, o **Número da Revisão** e a **Data da Revisão**. Clique em **Criar Checklist**. O modelo nasce em **Rascunho**.
{% endstep %}

{% step %}
### Crie uma seção

Clique no nome do modelo para abri-lo. Clique em **Nova Seção**, informe **Nome**, **Código**, **Ordem** e, se quiser, a **Descrição**, e clique em **Criar Seção**.
{% endstep %}

{% step %}
### Crie os itens

Clique em **Novo Item**. Informe o **Nome do Item**, o **Código** e o **Tipo do Item**. Se quiser, preencha a **Descrição do Item** e a **Ação Corretiva** e marque **Campo Obrigatório**. Clique em **Criar Item**.

<figure><img src="../.gitbook/assets/aud-modelo-custom-02.png" alt="Janela Novo Item com Nome do Item, Código, Tipo do Item, Campo Obrigatório e Ação Corretiva"><figcaption><p>Novo Item</p></figcaption></figure>
{% endstep %}

{% step %}
### Disponibilize

Quando terminar, clique em **Disponibilizar** e em **Confirmar**. Só então o modelo pode ser usado nas auditorias. Veja [Disponibilizar, revisar ou inativar um modelo](modelos/disponibilizar-modelo.md).
{% endstep %}
{% endstepper %}

## Deu errado?

{% hint style="warning" %}
**"Código é obrigatório"**: informe o código.
{% endhint %}

{% hint style="warning" %}
**"Nome é obrigatório"**: informe o nome.
{% endhint %}

{% hint style="warning" %}
**"Ocorreu um erro ao criar o checklist."**: tente de novo.
{% endhint %}

## Dúvidas comuns

<details>

<summary>Qual tipo de item escolher?</summary>

Veja [Escolher o tipo de item](modelos/tipos-de-item.md).

</details>

<details>

<summary>Como peço dados no início da auditoria?</summary>

Clique em **Editar Cabeçalhos** e em **Adicionar Campo de Cabeçalho**. Informe o **Nome do Campo**, o **Tipo** (Texto, Número, Data ou Sim/Não) e se é **Obrigatório**. Clique em **Salvar Cabeçalhos**. O auditor preenche esses campos ao criar a auditoria.

</details>

<details>

<summary>Dá para usar itens de NR aqui?</summary>

Sim. Na seção, clique em **Inluir NR na seção**, marque os itens, clique em **Incluir** e em **Confirmar**.

</details>

<details>

<summary>Por que não consigo editar o modelo?</summary>

Só dá para editar em **Rascunho** ou **Em Edição**. Se ele estiver **Disponível**, clique em **Colocar em Edição**.

</details>
