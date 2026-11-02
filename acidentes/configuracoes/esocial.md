---
description: Prepare o envio da CAT e do afastamento ao eSocial.
icon: building-shield
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

# Configurar o eSocial

**Para que serve:** preparar o GNRx para assinar e enviar ao eSocial a CAT (S-2210) e o afastamento (S-2230).

{% hint style="info" %}
**Quem pode fazer:** Gestor ou Administrador, com a permissão de enviar o certificado digital e configurar a transmissão ao eSocial.
{% endhint %}

## Antes de começar

* Tenha o certificado digital A1 da empresa (e-CNPJ ou e-CPF), em arquivo .pfx ou .p12, e a senha.

## Passo a passo

{% stepper %}
{% step %}
### Envie o certificado

Clique em **Configurações › eSocial**. Clique em **Enviar certificado**, escolha o arquivo e digite a **Senha do certificado**.

<figure><img src="../.gitbook/assets/config-esocial-01.png" alt="Tela eSocial com os passos Envie o certificado A1, Confira o empregador e Escolha o ambiente e ligue o envio"><figcaption><p>eSocial</p></figcaption></figure>
{% endstep %}

{% step %}
### Confira o empregador

Em **Novo empregador**, informe o nome e a **Raiz do CNPJ** (os 8 primeiros dígitos; o CNPJ completo só vale para órgão público). Escolha o certificado. Salve. Aparece "Empregador salvo.".
{% endstep %}

{% step %}
### Escolha o ambiente e ligue o envio

Comece em **Produção restrita (teste)**: não vale como entrega. Ligue **Transmitir pela GNRx**. Quando estiver tudo certo, use **Passar para produção** e digite PRODUÇÃO para confirmar.
{% endstep %}
{% endstepper %}

{% hint style="info" %}
Com o envio desligado, baixe o XML e informe o recibo do envio feito por fora.
{% endhint %}

## Deu errado?

| Mensagem na tela | O que fazer |
| --- | --- |
| "CNPJ inválido." | Use a raiz do CNPJ (8 dígitos). |
| "Outra raiz: a assinatura exige procuração eletrônica no e-CAC." | Use o certificado da própria empresa ou faça a procuração no e-CAC. |
| "Sem acesso à configuração do eSocial" | Peça a permissão de gerenciar certificados do eSocial. |

## Dúvidas comuns

<details>

<summary>Como tiro o certificado?</summary>

Clique em **Desativar** e confirme em **Desativar e apagar**. O arquivo e a senha são apagados da GNRx.

</details>

<details>

<summary>Tenho mais de um empregador.</summary>

Cadastre cada um em **Novo empregador**. Cada um pode usar o seu ambiente.

</details>
