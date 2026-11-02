---
description: No EPI, defina assinatura, envio por correio, notificação e ficha da unidade.
icon: sliders
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

# Configurar a unidade no EPI

**Para que serve:** definir, por unidade, como as entregas são assinadas e como sai a ficha de EPI.

{% hint style="info" %}
**Quem pode fazer:** quem abre a unidade no módulo Gestão de EPIs.
{% endhint %}

## Antes de começar

* Para a ficha, tenha o logo (JPG, PNG, SVG ou WEBP, até 5MB), o CNPJ e a razão social da unidade.

## Passo a passo

{% stepper %}
{% step %}
### Abra as configurações

Clique em **Estruturas › Unidades**. Na coluna **Ações**, clique no ícone de olho. Abra a aba **Configurações**.

<figure><img src="../../.gitbook/assets/unidades-config-01.png" alt="Aba Configurações da unidade com Assinatura Escrita, Envio por Correio, Notificação Automática de Assinatura na Entrega e Configuração da Ficha de EPI"><figcaption><p>Aba Configurações</p></figcaption></figure>
{% endstep %}

{% step %}
### Ajuste as entregas

* **Assinatura Escrita:** use **Desativar assinatura escrita** para aceitar só reconhecimento facial.
* **Envio por Correio:** ligado, a opção aparece na tela de entrega e o admin decide item a item.
* **Notificação Automática de Assinatura na Entrega:** escolha **Push (app)** para **Itens de EPI** e **Itens de outras categorias (produto)**.

Cada mudança mostra a mensagem de configuração atualizada.
{% endstep %}

{% step %}
### Configure a ficha de EPI

Em **Configuração da Ficha de EPI**, envie a **Logo Customizada** e preencha **CNPJ para Exibição** e **Razão Social para Exibição**. Clique em **Salvar Configuração**. Aparece "Configuração atualizada com sucesso!".
{% endstep %}
{% endstepper %}

## Deu errado?

| Mensagem na tela | O que fazer |
| --- | --- |
| "Formato inválido. Use JPG, PNG, SVG ou WEBP." | Troque o formato da imagem. |
| "Arquivo muito grande. Tamanho máximo: 5MB" | Use uma imagem menor. |
| "CNPJ deve conter 14 dígitos" | Confira o CNPJ. |

## Dúvidas comuns

<details>

<summary>A ficha da unidade fica diferente das outras?</summary>

Sim. Ao gerar a ficha, a unidade aparece como "(customizado)".

</details>

<details>

<summary>Saí sem salvar.</summary>

O aviso "Você tem alterações não salvas." lembra antes. Configure de novo e clique em **Salvar Configuração**.

</details>
