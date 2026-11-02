---
description: Registre o desligamento ou o afastamento de um colaborador, ou a volta dele.
icon: user-minus
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

# Desligar, afastar ou reativar um colaborador

**Para que serve:** registrar que a pessoa saiu da empresa, que está afastada por um tempo, ou que voltou.

{% hint style="info" %}
**Quem pode fazer:** Administrador, com a permissão de inativar colaboradores. Para reativar: Gestor ou Administrador, com a permissão de reativar colaboradores.
{% endhint %}

## Antes de começar

* Tenha o motivo do afastamento, se for o caso.

## Passo a passo

{% stepper %}
{% step %}
### Abra a inativação

Clique em **Estruturas › Colaboradores**. Na coluna **Ações**, abra o menu e clique em **Inativar**. Abre **Inativar colaborador**: "Escolha como deseja inativar este colaborador.".

<figure><img src="../../.gitbook/assets/colaboradores-inativar-01.png" alt="Janela Inativar colaborador com as opções Desligamento definitivo e Afastamento temporário"><figcaption><p>Inativar colaborador</p></figcaption></figure>
{% endstep %}

{% step %}
### Escolha o tipo

* **Desligamento definitivo:** encerra o vínculo, sem previsão de retorno.
* **Afastamento temporário:** a pessoa vai voltar. Escolha o **Motivo** (Alistamento militar, Licença maternidade, Licença paternidade, Licença médica, Licença sem vencimento ou Outro). Se quiser, informe a **Data prevista de retorno** e ligue **Reativar automaticamente nessa data**.

<figure><img src="../../.gitbook/assets/colaboradores-inativar-02.png" alt="Afastamento temporário com o Motivo, a Data prevista de retorno e a chave Reativar automaticamente nessa data"><figcaption><p>Afastamento temporário</p></figcaption></figure>
{% endstep %}

{% step %}
### Confirme

Clique em **Desligar colaborador** ou **Afastar colaborador**. Aparece "Colaborador inativado com sucesso!".
{% endstep %}

{% step %}
### Para reativar

Filtre por **Inativos** ou **Afastados**. Na coluna **Ações**, abra o menu e clique em **Reativar**. Na janela **Reativar colaborador**, clique em **Reativar**. Aparece "Colaborador reativado com sucesso!".
{% endstep %}
{% endstepper %}

## Deu errado?

O sistema pode mostrar avisos antes de confirmar:

| Mensagem na tela | O que fazer |
| --- | --- |
| "Este funcionário possui itens em aberto..." | Os itens continuam no histórico. Digite o nome do colaborador e clique em **Confirmar mesmo assim**. |
| "Este funcionário possui treinamentos em andamento..." | Os treinamentos continuam no histórico. Digite o nome e clique em **Confirmar mesmo assim**. |
| "Este funcionário tem estabilidade da CIPA..." | A dispensa sem justa causa é proibida. Escreva a **Justificativa do desligamento** e clique em **Justificar e desligar**, ou clique em **Manter colaborador**. |
| "Este funcionário tem estabilidade acidentária..." | Mesma coisa: justifique ou clique em **Manter colaborador**. |

## Dúvidas comuns

<details>

<summary>A pessoa volta sozinha do afastamento?</summary>

Só se você ligou **Reativar automaticamente nessa data**. Ela volta a ficar ativa no dia informado.

</details>

<details>

<summary>Perco o histórico ao inativar?</summary>

Não. O histórico continua guardado. O colaborador só deixa de entrar nos novos relatórios.

</details>
