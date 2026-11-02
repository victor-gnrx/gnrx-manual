---
description: Edite os dados, os participantes, as sessões e os arquivos da turma.
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

# Ajustar a turma

**Para que serve:** mudar os dados da turma, os participantes, as sessões e os arquivos.

{% hint style="info" %}
**Quem pode fazer:** Supervisor, Gestor ou Administrador, com a permissão de editar turmas.
{% endhint %}

## Antes de começar

* [Encontre a turma](encontrar-turma.md).

## Passo a passo

{% stepper %}
{% step %}
### Edite os dados

Clique em **Editar**. Em **Editar Treinamento**, ajuste nome, descrição, datas, **Presença mínima (%)** e **Informações de Custo**. Clique em **Salvar alterações**. Aparece "Treinamento atualizado com sucesso.".
{% endstep %}

{% step %}
### Ajuste os participantes

Em **Participantes**, clique em **Gerenciar**. Em **Adicionar Participantes**, busque por nome ou CPF e marque as pessoas. Para tirar alguém, use **Remover** na lista.

<figure><img src="../.gitbook/assets/turmas-participantes-01.png" alt="Painel Adicionar Participantes com a busca e a lista de colaboradores"><figcaption><p>Adicionar Participantes</p></figcaption></figure>
{% endstep %}

{% step %}
### Adicione uma sessão

Em **Sessões**, clique em **Nova sessão**. Informe **Data**, **Início** e **Fim**. A **Carga horária (h)** é calculada automaticamente. Clique em **Adicionar sessão**.
{% endstep %}

{% step %}
### Anexe arquivos

Clique em **Adicionar arquivo**. Escolha o tipo (**Documento**, **Imagem**, **Vídeo** ou **Certificado**), dê um nome (ex.: "Lista de presença - Turma Janeiro"), escolha a **Sessão** se quiser e envie.
{% endstep %}
{% endstepper %}

## Deu errado?

| Mensagem na tela | O que fazer |
| --- | --- |
| "Treinamento salvo com avisos" | Algumas sessões ficaram fora do novo período. Ajuste as sessões. |
| "Data de fim deve ser maior ou igual à data de início." | Confira as datas. |
| "Hora de fim deve ser maior que hora de início" | Confira os horários da sessão. |
| "Conflito com sessão do dia anterior." | Mude o horário da sessão. |

## Dúvidas comuns

<details>

<summary>Apareceu "Todos os colaboradores já estão no treinamento".</summary>

Não há mais ninguém para adicionar.

</details>

<details>

<summary>Posso mudar o instrutor?</summary>

Pode. Em **Instrutores**, clique em **Gerenciar** (ou **Adicionar Instrutor**).

</details>
