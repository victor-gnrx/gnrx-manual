---
description: "O rosto do colaborador confirma a entrega."
icon: face-smile
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

# Assinatura por reconhecimento facial

**Para que serve:** o colaborador assina a entrega olhando para a câmera.

{% hint style="info" %}
**Quem pode fazer:** Supervisor, Gestor ou Administrador, com a permissão de registrar entrega de EPIs.
{% endhint %}

## Antes de começar

* O item precisa estar entregue.
* O rosto do colaborador precisa estar cadastrado. Veja [Cadastrar o rosto do colaborador](../../configuracoes-iniciais/reconhecimento-facial/cadastrar-face.md).
* Use um equipamento com câmera.

## Passo a passo

{% stepper %}
{% step %}
### Abra a câmera

Abra a solicitação. Em **Recolher Assinatura**, clique em **Reconhecimento Facial**. Se tiver mais de uma câmera, use **Selecione a câmera**.

<figure><img src="../../.gitbook/assets/assinatura-facial-01.png" alt="Janela Reconhecimento Facial com a imagem da câmera e o botão Iniciar Captura"><figcaption><p>Reconhecimento Facial</p></figcaption></figure>
{% endstep %}

{% step %}
### Capture

Com o rosto do colaborador na tela, clique em **Iniciar Captura**. Aparece "Entrega Assinada com sucesso!".
{% endstep %}
{% endstepper %}

## Deu errado?

| Mensagem na tela | O que fazer |
| --- | --- |
| "Permissão negada" | Permita o acesso à câmera no navegador. |
| "Câmera não encontrada" | Conecte uma câmera. |
| "Câmera em uso" | Feche outros apps que usam a câmera. |
| "Contexto inseguro" | Use HTTPS para acessar a câmera. |

## Dúvidas comuns

<details>

<summary>O botão Reconhecimento Facial está apagado.</summary>

O item ainda não foi entregue ou o rosto do colaborador não está cadastrado.

</details>

<details>

<summary>Como sei como foi assinado?</summary>

Em **Detalhes da Assinatura**, aparece se foi com reconhecimento facial ou escrita.

</details>
