---
description: Ative e capture o rosto do colaborador.
icon: camera
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

# Cadastrar o rosto do colaborador

**Para que serve:** ativar e capturar o rosto do colaborador para ele assinar com reconhecimento facial.

{% hint style="info" %}
**Quem pode fazer:** Gestor ou Administrador, com a permissão de gerenciar reconhecimento facial.
{% endhint %}

## Antes de começar

* Use um computador com câmera e libere o acesso à câmera no navegador.
* Abra o colaborador: **Estruturas › Colaboradores**, menu da coluna **Ações**, **Visualizar**.

## Passo a passo

{% stepper %}
{% step %}
### Ative (se pedir)

Se aparecer **Ativar reconhecimento facial**, clique nele. Em **Confirmar Ativação**, clique em **Ativar**. Aparece "Ativação realizada com sucesso!".
{% endstep %}

{% step %}
### Abra o cadastro

Na linha **Rec. Facial**, clique em **Cadastrar** (ou **Editar**, para trocar). Abre **Cadastro Facial**.

<figure><img src="../../.gitbook/assets/colaboradores-facial-01.png" alt="Tela Cadastro Facial com a escolha da câmera, o oval para o rosto e os botões Iniciar Captura e Finalizar Cadastro"><figcaption><p>Cadastro Facial</p></figcaption></figure>
{% endstep %}

{% step %}
### Capture o rosto

Escolha a câmera e clique em **Iniciar Captura**. Siga as orientações: "Posicione seu rosto dentro do oval", "Aproxime-se da câmera", "Afaste-se um pouco da câmera", "Segure a posição". Ou clique em **Capturar Agora**.
{% endstep %}

{% step %}
### Finalize

Clique em **Finalizar Cadastro**. Aparece "Reconhecimento facial atualizado com sucesso!".
{% endstep %}
{% endstepper %}

## Deu errado?

| Mensagem na tela | O que fazer |
| --- | --- |
| "Não foi possível acessar as câmeras." | Libere a câmera no navegador e confira se ela está conectada. |
| "Câmera desconectada" | Reconecte a câmera e escolha de novo. |

## Dúvidas comuns

<details>

<summary>Como tiro o reconhecimento facial?</summary>

Na linha **Rec. Facial**, clique em **Remover** e confirme em **Remover Reconhecimento Facial**.

</details>

<details>

<summary>O que acontece ao remover?</summary>

O sistema avisa: "Após esta alteração, o colaborador não poderá mais solicitar EPIs.".

</details>
