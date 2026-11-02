---
description: Defina prazos, custo-hora, a gestão da CAT e os alertas.
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

# Ajustar as configurações gerais

**Para que serve:** definir os prazos de investigação, a verificação de eficácia, como a CAT é emitida, o custo-hora, os alertas e o registro anônimo.

{% hint style="info" %}
**Quem pode fazer:** Gestor ou Administrador, com a permissão de editar as configurações do módulo.
{% endhint %}

## Antes de começar

* Cada unidade pode ter os seus valores. O que você define aqui é o padrão da empresa.

## Passo a passo

{% stepper %}
{% step %}
### Abra as configurações

Clique em **Configurações › Geral**. Abre **Configurações gerais**.

<figure><img src="../.gitbook/assets/config-geral-01.png" alt="Configurações gerais com Prazo da investigação por gravidade, Verificação de eficácia, Gestão da CAT e Custo-hora"><figcaption><p>Configurações gerais</p></figcaption></figure>
{% endstep %}

{% step %}
### Ajuste os prazos

Em **Prazo da investigação por gravidade**, informe os dias de cada gravidade (de 0 a 365). A triagem sugere o prazo pela maior gravidade, real ou potencial. Em **Verificação de eficácia**, informe os dias contados da conclusão da ocorrência (de 1 a 730).
{% endstep %}

{% step %}
### Escolha a gestão da CAT

Em **Gestão da CAT**, escolha:

* **Pelo GNRx:** abre, controla o prazo e transmite ao eSocial;
* **Emissão externa:** o RH ou outro sistema emite; aqui fica só o número da CAT.
{% endstep %}

{% step %}
### Custo-hora, alertas e registro anônimo

Informe o **Custo-hora padrão da empresa**. Em **Alertas e registro**, cadastre os **E-mails da empresa** (recebem os alertas de todas as unidades). Em **Registro anônimo**, a opção prepara um canal que ainda não está disponível: hoje as ocorrências são registradas pelo painel. Clique em **Salvar**. Aparece "Configuração salva.".
{% endstep %}
{% endstepper %}

{% hint style="info" %}
**Por unidade:** em **Por unidade**, clique em **Personalizar** para dar valores próprios a uma unidade, ou **Usar os da empresa** para voltar ao padrão.
{% endhint %}

## Deu errado?

| Mensagem na tela | O que fazer |
| --- | --- |
| "Cada prazo vai de 0 a 365 dias." | Ajuste o prazo. |
| "Informe de 1 a 730 dias." | Ajuste os dias da verificação de eficácia. |

## Dúvidas comuns

<details>

<summary>Alguém quer comunicar algo sem se identificar.</summary>

Hoje não há canal anônimo de ocorrência. Para denunciar sem se identificar, use a denúncia da CIPA.

</details>

<details>

<summary>Ocorrência sem unidade avisa quem?</summary>

Os e-mails da empresa. Sem e-mail da empresa, ocorrências sem unidade não avisam ninguém.

</details>
