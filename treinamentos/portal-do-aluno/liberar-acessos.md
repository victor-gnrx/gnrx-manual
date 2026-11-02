---
description: Diga quem vê cada curso ou vitrine do portal.
icon: key
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

# Liberar os acessos aos cursos

**Para que serve:** dizer quem vê cada curso ou vitrine no portal, e o que é obrigatório.

{% hint style="info" %}
**Quem pode fazer:** Supervisor, Gestor ou Administrador, com a permissão de gerenciar o conteúdo do EAD.
{% endhint %}

## Antes de começar

* [Crie o portal](criar-portal.md) e publique os cursos.

## Passo a passo

{% stepper %}
{% step %}
### Escolha o curso ou a vitrine

Na aba **Acessos**, escolha um curso ou uma vitrine à esquerda.

<figure><img src="../.gitbook/assets/portal-acessos-01.png" alt="Aba Acessos com a lista de cursos e vitrines e as regras de acesso"><figcaption><p>Aba Acessos</p></figcaption></figure>
{% endstep %}

{% step %}
### Adicione as regras

Clique em **Adicionar regra** e escolha quem vê: todos os colaboradores ativos, uma unidade, um setor, um cargo, um GHE / Grupo ou um colaborador. Marque **Obrigatório** e o **Prazo em dias** (de 1 a 3650), se for o caso.
{% endstep %}

{% step %}
### Salve

Clique em **Salvar acessos**. Aparece "Acessos salvos.".
{% endstep %}
{% endstepper %}

{% hint style="info" %}
**Pela matriz de GHE:** ligue **Usar a matriz de GHE / Grupo para os obrigatórios**. O curso de cada treinamento obrigatório no GHE do colaborador entra como obrigatório para ele.
{% endhint %}

## Deu errado?

| Mensagem na tela | O que fazer |
| --- | --- |
| "Há regra repetida." | Tire a regra duplicada. |
| "O prazo vai de 1 a 3650 dias." | Ajuste o prazo. |

## Dúvidas comuns

<details>

<summary>Curso sem regra aparece para alguém?</summary>

Só para quem tem acesso por uma vitrine. Vitrine sem regra não libera curso para ninguém.

</details>

<details>

<summary>Obrigatório sem prazo atrasa?</summary>

Não. Sem prazo, o curso aparece em Obrigatórios, sem atrasar.

</details>
