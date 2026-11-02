---
description: Bloqueie o acesso de um usuário ou devolva o acesso a ele.
icon: user-slash
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

# Inativar ou reativar um usuário

**Para que serve:** bloquear o acesso de quem saiu da empresa ou devolver o acesso depois.

{% hint style="info" %}
**Quem pode fazer:** Administrador, com a permissão de inativar usuários (para reativar, a permissão de reativar usuários).
{% endhint %}

## Antes de começar

* Nada a preparar. O histórico do usuário continua guardado.

## Passo a passo

{% stepper %}
{% step %}
### Encontre o usuário

Clique em **Estruturas › Usuários**. Para achar alguém já inativo, use o filtro **Ativo/Inativo**.

<figure><img src="../../.gitbook/assets/usuarios-inativar-01.png" alt="Lista de usuários com o filtro Ativo/Inativo e a coluna Ações"><figcaption><p>Lista com filtro Ativo/Inativo</p></figcaption></figure>
{% endstep %}

{% step %}
### Inative

Na coluna **Ações**, escolha inativar. Aparece o aviso: "Esta ação irá inativar o usuário. Ele não poderá mais acessar o sistema até ser reativado."

<figure><img src="../../.gitbook/assets/usuarios-inativar-02.png" alt="Janela de confirmação da inativação do usuário"><figcaption><p>Confirmação da inativação</p></figcaption></figure>
{% endstep %}

{% step %}
### Confirme

Confirme. Aparece **Usuário inativado**. Para reativar, faça o mesmo caminho.
{% endstep %}
{% endstepper %}

## Dúvidas comuns

<details>

<summary>A pessoa é desconectada na hora?</summary>

O bloqueio vale a partir do próximo acesso.

</details>

<details>

<summary>Dá para excluir o usuário de vez?</summary>

Não. Só existe inativar e reativar.

</details>
