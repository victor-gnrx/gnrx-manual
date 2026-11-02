---
description: Corrija os dados de contato de uma empresa terceira.
icon: pen
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

# Editar uma empresa terceira

**Para que serve:** corrigir nome, contato e responsável de uma empresa terceira.

{% hint style="info" %}
**Quem pode fazer:** Gestor ou Administrador, com a permissão de editar terceiros.
{% endhint %}

## Antes de começar

* O CNPJ e o CPF não podem ser alterados.

## Passo a passo

{% stepper %}
{% step %}
### Abra a empresa

Clique em **Estruturas › Terceiros** e depois em **Ver** na empresa. No topo, clique em **Editar**. Abre **Editar Empresa Terceira**.

<figure><img src="../../.gitbook/assets/terceiros-editar-01.png" alt="Janela Editar Empresa Terceira com o CNPJ bloqueado e os demais campos editáveis"><figcaption><p>Janela Editar Empresa Terceira</p></figcaption></figure>
{% endstep %}

{% step %}
### Corrija e salve

Altere o que precisar e clique em **Salvar Alterações**. Aparece "Empresa terceira atualizada com sucesso.".
{% endstep %}
{% endstepper %}

## Deu errado?

| Mensagem na tela | O que fazer |
| --- | --- |
| "Nome é obrigatório" | Preencha o nome. |
| "Email deve ter formato válido" ou "Email do responsável deve ter formato válido" | Confira o e-mail (ex.: email@empresa.com). |
| "Nome deve ter no máximo 255 caracteres" | Encurte o nome. O mesmo vale para nome fantasia e nome do responsável. |
| "Telefone deve ter no máximo 20 caracteres" | Confira o telefone. O mesmo vale para o telefone do responsável. |
| "Endereço deve ter no máximo 500 caracteres" | Encurte o endereço. |

## Dúvidas comuns

<details>

<summary>Por que não consigo mudar o CNPJ?</summary>

O CNPJ e o CPF ficam bloqueados depois de criados.

</details>

<details>

<summary>Posso editar uma empresa inativa?</summary>

Não. O botão **Editar** só aparece em empresa ativa. Veja [Inativar ou reativar](inativar-terceiro.md).

</details>
