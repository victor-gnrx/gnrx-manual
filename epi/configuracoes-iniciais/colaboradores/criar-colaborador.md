---
description: Cadastre uma pessoa que trabalha na empresa.
icon: user-plus
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

# Criar um colaborador

**Para que serve:** cadastrar uma pessoa que trabalha na empresa.

{% hint style="info" %}
**Quem pode fazer:** Administrador, com a permissão de cadastrar colaboradores.
{% endhint %}

## Antes de começar

* Tenha o nome e o CPF da pessoa.
* Para um terceiro, cadastre antes a [empresa terceira](../terceiros/criar-terceiro.md) e crie o colaborador de dentro dela.

## Passo a passo

{% stepper %}
{% step %}
### Clique em Novo colaborador

Clique em **Estruturas › Colaboradores** e depois em **Novo colaborador**. Abre a janela **Criar colaborador** (ou **Criar colaborador terceiro**, se você estiver dentro de uma empresa terceira).

<figure><img src="../../.gitbook/assets/colaboradores-criar-01.png" alt="Janela Criar colaborador com os campos Nome, Email, CPF, telefone, Matrícula, Início da Atividade, Turno e Pin de Acesso"><figcaption><p>Janela Criar colaborador</p></figcaption></figure>
{% endstep %}

{% step %}
### Preencha os dados

* **Nome:** obrigatório, até 128 caracteres.
* **CPF:** obrigatório.
* **Pin de Acesso:** é a senha de 6 números do colaborador no aplicativo e no Portal do Aluno.
* **Email**, telefone, **Matrícula** (até 20 caracteres), **Início da Atividade** e **Turno**: opcionais.

No **Turno**, escolha um turno ou digite um nome novo. O nome novo vira um [turno](../turnos/README.md).
{% endstep %}

{% step %}
### Salve

Clique em **Salvar**. Aparece "Colaborador criado com sucesso".
{% endstep %}
{% endstepper %}

Depois, [vincule a unidade](vincular-unidades.md) e o [setor e o cargo](vincular-setores.md).

## Deu errado?

| Mensagem na tela | O que fazer |
| --- | --- |
| "Nome é obrigatório" | Preencha o nome. |
| "CPF inválido" | Confira o CPF (11 números). |
| "Senha deve ter 6 números" | O Pin de Acesso precisa ter 6 números. |
| "Email inválido" | Confira o e-mail. |
| "Data adesão inválida" | O início da atividade não pode ser no futuro. |
| "Limite Atingido" | O plano chegou ao limite de colaboradores ativos. Fale com o seu contato comercial da GNRx. |

## Dúvidas comuns

<details>

<summary>Posso criar sem e-mail?</summary>

Pode. O e-mail é opcional.

</details>

<details>

<summary>Vale para todos os módulos?</summary>

Sim. O colaborador é o mesmo em todos os módulos do GNRx.

</details>
