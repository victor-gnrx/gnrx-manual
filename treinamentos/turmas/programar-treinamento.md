---
description: Crie uma turma de treinamento em 5 etapas.
icon: calendar-plus
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

# Programar um treinamento

**Para que serve:** criar uma turma: qual treinamento, quando, quem participa e quem ministra.

{% hint style="info" %}
**Quem pode fazer:** Gestor ou Administrador, com a permissão de criar treinamentos.
{% endhint %}

## Antes de começar

* O tipo de treinamento precisa estar no catálogo (**Configurações › Tipos de Treinamentos**).
* Cadastre os [instrutores](../estruturas/instrutores/criar-instrutor.md) e os [colaboradores](../estruturas/colaboradores/criar-colaborador.md).

## Passo a passo

{% stepper %}
{% step %}
### Informações básicas

Clique em **Turmas › Novo Treinamento**. Em **Tipo de treinamento**, busque pelo nome ou código. O nome da turma começa com o nome do treinamento e pode ser mudado. Escolha a **Unidade** (em branco = **Empresa toda**), a **Modalidade** (**Presencial**, **EAD** ou **Semipresencial**), o **Custo total** e a **Presença mínima** (ou **Sem mínimo**). No EAD e no semipresencial, informe **Abre em** e **Prazo para concluir**.

<figure><img src="../.gitbook/assets/turmas-programar-01.png" alt="Etapa Informações básicas com Tipo de treinamento, Unidade, Nome da turma, Modalidade e Presença mínima"><figcaption><p>Informações básicas</p></figcaption></figure>
{% endstep %}

{% step %}
### Sessões

Clique em **Adicionar sessão** e informe **Data**, **Início** e **Fim**. **Repetir no próximo dia útil** copia a sessão. No EAD, as sessões são opcionais.

<figure><img src="../.gitbook/assets/turmas-programar-02.png" alt="Etapa Sessões com a lista de sessões e o botão Adicionar sessão"><figcaption><p>Sessões</p></figcaption></figure>
{% endstep %}

{% step %}
### Participantes

Busque por nome, CPF, matrícula ou e-mail e marque quem vai fazer o treinamento. Só aparecem colaboradores ativos.
{% endstep %}

{% step %}
### Instrutores

Marque quem ministra e clique em **Tornar principal** em um deles. O principal aparece no certificado e na lista de presença. No EAD, o instrutor é opcional.
{% endstep %}

{% step %}
### Revisão

Confira tudo. Para voltar a uma etapa, clique em **Alterar**. Clique em **Programar treinamento**. A turma é criada e abre a página dela.

<figure><img src="../.gitbook/assets/turmas-programar-03.png" alt="Etapa Revisão com o resumo da turma e o botão Programar treinamento"><figcaption><p>Revisão</p></figcaption></figure>
{% endstep %}
{% endstepper %}

## Deu errado?

| Mensagem na tela | O que fazer |
| --- | --- |
| "Escolha o tipo de treinamento." | Busque e escolha o treinamento. |
| "Dê um nome à turma." | Preencha o nome. |
| "Adicione pelo menos uma sessão." | No presencial, cadastre ao menos uma sessão. |
| "Selecione pelo menos um participante." | Marque os participantes. |
| "Selecione pelo menos um instrutor." / "Marque um instrutor como principal." | Escolha os instrutores e clique em **Tornar principal**. |
| "O prazo para concluir precisa vir depois da abertura." | Confira as datas. |
| "O fim precisa vir depois do início." | Confira os horários da sessão. |

## Dúvidas comuns

<details>

<summary>Sou Supervisor e não consigo programar.</summary>

Programar exige a permissão de criar treinamentos. Peça ao administrador.

</details>

<details>

<summary>O que a presença mínima faz?</summary>

É o percentual das sessões que o participante precisa ter para ser aprovado. Sem mínimo, a presença não reprova.

</details>

<details>

<summary>O instrutor não aparece na lista.</summary>

Clique em **Cadastrar instrutor** e depois em **Atualizar a lista**.

</details>
