---
description: Cadastre os documentos que a empresa exige e por quanto tempo valem.
icon: file-lines
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

# Cadastrar um tipo de documento

**Para que serve:** dizer quais documentos a empresa exige, de quem e por quanto tempo valem.

{% hint style="info" %}
**Quem pode fazer:** Gestor ou Administrador, com a permissão de criar tipos de documento.
{% endhint %}

## Antes de começar

* Comece pelo catálogo padrão: ele já traz os documentos mais comuns, prontos para ajustar.

## Passo a passo

{% stepper %}
{% step %}
### Use o catálogo ou crie

Clique em **Configurações › Tipos de documento**. Clique em **Catálogo padrão**, marque os documentos e clique em **Adicionar à empresa**. Ou clique em **Novo tipo**.

<figure><img src="../.gitbook/assets/docs-tipos-01.png" alt="Tela Tipos de documento com a lista e os botões Novo tipo e Catálogo padrão"><figcaption><p>Tipos de documento</p></figcaption></figure>
{% endstep %}

{% step %}
### Preencha

Informe o nome (ex.: Atestado de Saúde Ocupacional (ASO)), a categoria e a quem **Se aplica a**. Em **Validade e alertas**, informe a validade em dias e quando avisar. Em **Análise e regras**, decida se é **Obrigatório por padrão** e se é **Dado sensível (LGPD)**. Se quiser, escreva as **Instruções de envio** e anexe um **Arquivo de exemplo**.
{% endstep %}

{% step %}
### Salve

Clique em **Salvar tipo**. Aparece "Tipo criado.".
{% endstep %}
{% endstepper %}

## Deu errado?

| Mensagem na tela | O que fazer |
| --- | --- |
| "Informe o nome." / "Informe a categoria." | Preencha. |
| "Escolha a quem o documento se aplica." | Marque um ou mais. |
| "Informe a validade em dias." | Preencha a validade. |
| "O dia limite da competência vai de 1 a 28." | Ajuste o dia. |

## Dúvidas comuns

<details>

<summary>Um certificado de treinamento vale como documento?</summary>

Vale. Em **Treinamentos que cumprem**, escolha os treinamentos cujo certificado vale como este documento.

</details>

<details>

<summary>O que muda se eu marcar Dado sensível?</summary>

Abrir o arquivo exige permissão própria, e cada abertura fica registrada.

</details>
