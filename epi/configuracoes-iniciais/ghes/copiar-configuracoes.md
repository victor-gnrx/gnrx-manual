---
description: Copie riscos, EPIs, prazos e certificações de outro GHE.
icon: copy
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

# Copiar a configuração de outro GHE

**Para que serve:** reaproveitar riscos, EPIs, tempos de troca e certificações de um GHE parecido.

{% hint style="info" %}
**Quem pode fazer:** Gestor ou Administrador, com a permissão de associar EPIs aos GHEs.
{% endhint %}

## Antes de começar

* Tenha um GHE já configurado para usar como origem.

{% hint style="warning" %}
As configurações atuais do GHE são **substituídas** pelas do GHE de origem. Não dá para desfazer.
{% endhint %}

## Passo a passo

{% stepper %}
{% step %}
### Abra a cópia

No GHE, clique em **Copiar de outro GHE**. Abre **Clonar Configurações de Grupo**.

<figure><img src="../../.gitbook/assets/ghe-copiar-01.png" alt="Janela Clonar Configurações de Grupo com Filtrar por Unidade, Grupo de Origem e o aviso de que as configurações serão substituídas"><figcaption><p>Clonar Configurações de Grupo</p></figcaption></figure>
{% endstep %}

{% step %}
### Escolha a origem

Se quiser, use **Filtrar por Unidade**. Em **Grupo de Origem**, escolha o GHE. Leia o aviso.
{% endstep %}

{% step %}
### Confirme

Clique em **Clonar Configurações**. Aparece "Configurações copiadas".
{% endstep %}
{% endstepper %}

## Dúvidas comuns

<details>

<summary>Os colaboradores também são copiados?</summary>

Não. São copiados riscos, EPIs, tempos de troca e certificações.

</details>

<details>

<summary>Posso copiar ao criar o GHE?</summary>

Pode. Use **Copiar configurações de outro grupo** na janela **Criar Novo Grupo**.

</details>
