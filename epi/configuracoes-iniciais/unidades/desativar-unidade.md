---
description: Tire da lista uma unidade que não existe mais.
icon: ban
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

# Inativar uma unidade

**Para que serve:** tirar da lista uma unidade que a empresa não usa mais.

{% hint style="info" %}
**Quem pode fazer:** Administrador, com a permissão de inativar unidades.
{% endhint %}

## Antes de começar

* Confira se a unidade é mesmo a certa. Use a [busca](listar-unidades.md).
* Veja quais usuários têm só essa unidade. Depois de inativar, eles perdem o vínculo com ela.

## O que acontece ao inativar

* **Usuários:** quem tinha essa unidade perde o vínculo com ela. Quem só tinha essa unidade passa a **não ver nada** até o administrador [vincular outra unidade](../usuarios/vincular-unidades.md).
* **Colaboradores e setores:** continuam vinculados à unidade.
* **GHEs da unidade** (Gestão de EPIs): são inativados junto.

## Passo a passo

{% hint style="warning" %}
Atenção: depois de inativar, não dá para reativar pelo sistema. Se inativou por engano, abra um [chamado no Suporte](../../suporte/abrir-chamado.md).
{% endhint %}

{% stepper %}
{% step %}
### Clique na lixeira

Clique em **Estruturas › Unidades**. Na coluna **Ações**, clique no ícone de lixeira. Abre **Inativar Unidade**: "Tem certeza que deseja inativar esta unidade?".

<figure><img src="../../.gitbook/assets/unidades-inativar-01.png" alt="Janela Inativar Unidade com a pergunta de confirmação e os botões Cancelar e Inativar"><figcaption><p>Inativar Unidade</p></figcaption></figure>
{% endstep %}

{% step %}
### Confirme

Clique em **Inativar**. A unidade passa a aparecer como **Inativo**.
{% endstep %}
{% endstepper %}

## Dúvidas comuns

<details>

<summary>A mensagem diz "excluída". A unidade foi apagada?</summary>

Não. A unidade fica inativa e continua na lista com o status **Inativo**.

</details>

<details>

<summary>Algo impede a inativação?</summary>

Não. A unidade pode ser inativada mesmo com colaboradores, setores e usuários vinculados.

</details>

<details>

<summary>Posso editar uma unidade inativa?</summary>

Não. Os ícones de lápis e de lixeira ficam apagados.

</details>
