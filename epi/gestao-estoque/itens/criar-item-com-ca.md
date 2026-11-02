---
description: Cadastre um EPI com CA, preenchendo pelo número do CA.
icon: helmet-safety
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

# Cadastrar um EPI

**Para que serve:** cadastrar um EPI com Certificado de Aprovação (CA) no inventário.

{% hint style="info" %}
**Quem pode fazer:** Gestor ou Administrador, com a permissão de cadastrar novos itens de EPI.
{% endhint %}

## Antes de começar

* Tenha o número do CA.

## Passo a passo

{% stepper %}
{% step %}
### Clique em Novo Item

Clique em **Inventário › Gerenciar Inventário** e depois em **Novo Item**. Escolha **EPI** (equipamento com CA obrigatório).

<figure><img src="../../.gitbook/assets/inventario-criar-epi-01.png" alt="Janela Criar EPI com Nome, Número CA, Data de Validade, EPI (NR-6), Tempo de Troca e Fabricante"><figcaption><p>Criar EPI</p></figcaption></figure>
{% endstep %}

{% step %}
### Preencha pelo CA (opcional)

Use **Buscar CA EPI**: digite o número do CA (mín. 3 dígitos). Aparece "Dados preenchidos automaticamente". Se o fabricante não existir, use **Criar Novo**.
{% endstep %}

{% step %}
### Complete os dados

Confira **Nome**, **Número CA**, **Data de Validade**, **EPI (NR-6)**, **Tempo de Troca (Dias)** e **Fabricante**. Escolha se rastreia cada unidade (**Controle Unitário**) ou só a quantidade, e se é **Sem devolução** (descartável).
{% endstep %}

{% step %}
### Salve

Clique em **Salvar EPI**. Aparece "EPI criado com sucesso".
{% endstep %}
{% endstepper %}

## Deu errado?

| Mensagem na tela | O que fazer |
| --- | --- |
| "Selecione pelo menos um EPI (NR-6)" | Escolha o tipo de EPI. |
| "Fabricante é obrigatório" | Escolha ou crie o fabricante. |
| "Data de validade é obrigatória quando há número CA" | Informe a validade do CA. |
| "Sem devolução não pode ser ativado com controle unitário" | Desligue um dos dois. |
| "CA não encontrado" | Confira o número ou preencha à mão. |

## Dúvidas comuns

<details>

<summary>Tenho muitos EPIs para cadastrar.</summary>

Use **Ações › Importar Itens por CA**. Veja [Importar itens por CA](importar-por-ca.md).

</details>

<details>

<summary>E depois de cadastrar?</summary>

[Dê entrada no estoque](adicionar-lote.md).

</details>
