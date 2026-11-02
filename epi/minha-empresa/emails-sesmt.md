---
description: Defina quais e-mails recebem os avisos de EPI, CIPA e acidentes.
icon: envelope
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

# Cadastrar os e-mails do SESMT

**Para que serve:** definir quem recebe os avisos automáticos do GNRx.

{% hint style="info" %}
**Quem pode fazer:** só o acesso Empresa (CNPJ).
{% endhint %}

## Antes de começar

* A sua empresa precisa ter o módulo Gestão de EPIs. Sem ele, o bloco **E-mails SESMT** não aparece.
* Tenha a lista de e-mails da equipe de segurança do trabalho.

## Passo a passo

{% stepper %}
{% step %}
### Abra a aba E-mails

No menu do usuário, clique em **Minha Empresa** e depois na aba **E-mails**.
{% endstep %}

{% step %}
### Informe os e-mails

Em **E-mails SESMT**, digite um e-mail no campo (ex.: sesmt@empresa.com.br) e clique em **Adicionar**. Aparece "E-mail adicionado.". Repita para cada e-mail. Não há botão de salvar: cada e-mail vale assim que é adicionado.

Para tirar um e-mail, clique em remover ao lado dele. Aparece "E-mail removido destes alertas.".

{% hint style="info" %}
Se aparecer "Nenhum e-mail da empresa recebe estes alertas.", a lista está vazia e ninguém recebe os avisos.
{% endhint %}

<figure><img src="../.gitbook/assets/empresa-06-emails.png" alt="Aba E-mails com a lista E-mails SESMT preenchida"><figcaption><p>E-mails SESMT</p></figcaption></figure>
{% endstep %}
{% endstepper %}

## Dúvidas comuns

<details>

<summary>Que avisos esses e-mails recebem?</summary>

Os avisos de CA inválido e de validade informada pelo fabricante, da Gestão de EPIs. A Gestão de CIPA e a Gestão de Acidentes usam a mesma lista para os avisos delas.

</details>

<details>

<summary>Posso cadastrar mais de um e-mail?</summary>

Pode. Cadastre todos que devem receber os avisos.

</details>
