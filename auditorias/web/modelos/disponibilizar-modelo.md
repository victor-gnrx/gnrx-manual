---
description: "Libere o modelo para as auditorias, altere, crie uma nova versão ou inative."
icon: circle-check
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

# Disponibilizar, revisar ou inativar um modelo

**Para que serve:** liberar um modelo customizado para as auditorias e, depois, alterar ou tirar de uso.

{% hint style="info" %}
**Quem pode fazer:** Gestor ou Administrador, com a permissão de editar modelos. Criar uma nova versão pede a permissão de criar modelos. Inativar pede a permissão de excluir modelos.
{% endhint %}

## Antes de começar

* Tenha um [modelo customizado](../modelo-customizado.md) criado.

## Os estados do modelo

| Estado | O que significa |
| --- | --- |
| **Rascunho** | Em montagem. Ainda não vai para as auditorias. |
| **Disponível** | Liberado para as auditorias. Não dá para editar. |
| **Em Edição** | Sendo alterado depois de disponível. |

## Passo a passo

{% stepper %}
{% step %}
### Abra o modelo

Clique em **Modelos Customizados** e no nome do modelo.

<figure><img src="../../.gitbook/assets/aud-modelo-estado-01.png" alt="Modelo customizado aberto com o estado e os botões Disponibilizar e Excluir"><figcaption><p>Modelo aberto</p></figcaption></figure>
{% endstep %}

{% step %}
### Disponibilize

Clique em **Disponibilizar** e em **Confirmar**. O modelo fica **Disponível**.
{% endstep %}

{% step %}
### Para alterar

Clique em **Colocar em Edição** e em **Confirmar**. Faça as mudanças e clique em **Disponibilizar** de novo.
{% endstep %}
{% endstepper %}

## Dúvidas comuns

<details>

<summary>Como crio uma nova versão sem mexer na atual?</summary>

Em **Modelos Customizados**, abra o menu da linha de um modelo **Disponível** e clique em **Clonar Modelo** e em **Confirmar e Clonar**. Depois clique em **Abrir Modelo**.

</details>

<details>

<summary>Como tiro o modelo de uso?</summary>

Dentro do modelo, clique em **Excluir** e em **Inativar**. Ou use **Inativar** no menu da linha. O modelo vai para **Inativos**.

</details>

<details>

<summary>Como levo o modelo para o Excel?</summary>

Dentro do modelo, clique em **Exportar Excel** e escolha **Planilha de Preenchimento** ou **Estrutura Detalhada**.

</details>
