---
description: Cadastre riscos críticos, equipamentos, processos, classificações e faixas de custo.
icon: layer-group
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

# Ajustar os catálogos

**Para que serve:** cadastrar os riscos críticos, os tipos de equipamento, os processos, as classificações e as faixas de custo da empresa.

{% hint style="info" %}
**Quem pode fazer:** Gestor ou Administrador, com a permissão de editar as configurações do módulo.
{% endhint %}

## Antes de começar

* Os itens de origem **Sistema** já cobrem os casos mais comuns. Crie só o que é próprio da empresa.

## Passo a passo

{% stepper %}
{% step %}
### Abra os catálogos

Clique em **Configurações › Catálogos**.

<figure><img src="../.gitbook/assets/config-catalogos-01.png" alt="Tela Catálogos com Riscos críticos, Tipos de equipamento, processos, classificações e Faixas de custo"><figcaption><p>Catálogos</p></figcaption></figure>
{% endstep %}

{% step %}
### Cadastre o que precisa

* **Riscos críticos** (**Novo risco crítico**): os riscos que podem matar ou incapacitar.
* **Tipos de equipamento** (**Novo tipo de equipamento**): a identificação (placa, TAG) vai na ocorrência.
* **Processos** (**Novo processo**): as atividades da operação, como carregamento.
* **Classificações** (**Nova classificação**): a gravidade de cada caso. Diga se **Conta como caso registrável (TRIFR)**.
* **Faixas de custo** (**Nova faixa**): os limites crescem de uma faixa para a outra.
{% endstep %}

{% step %}
### Salve

Preencha e salve.
{% endstep %}
{% endstepper %}

## Deu errado?

| Mensagem na tela | O que fazer |
| --- | --- |
| "Os limites precisam crescer de uma faixa para a outra." | Ajuste os limites. |
| "Só a última faixa fica sem limite." | Dê limite às outras faixas. |
| "Dê um nome a cada faixa." | Preencha os nomes. |

## Dúvidas comuns

<details>

<summary>Como tiro um item?</summary>

Use **Inativar**. Para trazer de volta, abra **Inativos** e clique em **Reativar**.

</details>

<details>

<summary>Errei as faixas de custo.</summary>

Clique em **Voltar ao padrão**. Aparece "Faixas padrão de volta.".

</details>
