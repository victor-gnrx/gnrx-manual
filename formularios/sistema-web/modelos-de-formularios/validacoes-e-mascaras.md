---
description: "Limite os valores de um campo e defina a máscara."
icon: shield-check
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

# Configurar validação e máscara de um campo

**Para que serve:** avisar ou impedir quando um valor sai do esperado (ex.: temperatura acima de 8) e padronizar o formato do campo.

{% hint style="info" %}
**Quem pode fazer:** Gestor ou Administrador, com a permissão de criar ou editar modelos de formulário.
{% endhint %}

## Antes de começar

* O campo precisa estar no modelo. Veja [Adicionar campos ao modelo](editor-de-campos.md).

## Passo a passo

{% stepper %}
{% step %}
### Abra as validações do campo

No campo, abra **Validações do Campo** e clique em **Adicionar nova regra**.

<figure><img src="../../.gitbook/assets/form-validacoes-01.png" alt="Janela Validações do Campo com Validação, Valor e Tipo de Validação (Alerta ou Obrigatório)"><figcaption><p>Validações do Campo</p></figcaption></figure>
{% endstep %}

{% step %}
### Defina a regra

Em **Validação**, escolha **Valor maior que** ou **Valor menor que** e informe o **Valor**. Em **Tipo de Validação**, escolha o nível: **Alerta** (aviso visual, permite continuar) ou **Obrigatório** (impede salvamento). Clique em **Adicionar**.
{% endstep %}

{% step %}
### Defina a máscara (se quiser)

Em **Máscara/Opções/Padrão Obs.**, informe a máscara do campo. Clique em **Salvar Modelo**.
{% endstep %}
{% endstepper %}

## Dúvidas comuns

<details>

<summary>Posso pôr dois limites?</summary>

Pode: um **Valor maior que** e um **Valor menor que** no mesmo campo, cada um uma vez.

</details>

<details>

<summary>O que a equipe vê?</summary>

Com **Alerta**, um aviso e o registro é salvo. Com **Obrigatório**, o registro não é salvo até corrigir.

</details>
