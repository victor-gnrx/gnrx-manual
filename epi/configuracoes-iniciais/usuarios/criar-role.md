---
description: Monte uma role com as permissões que a sua empresa precisa.
icon: user-shield
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

# Criar uma role

**Para que serve:** montar uma role com as permissões que a sua empresa precisa, quando nenhuma das padrão serve.

{% hint style="info" %}
**Quem pode fazer:** Administrador, com a permissão de criar roles.
{% endhint %}

## Antes de começar

* Veja se uma role padrão já serve: [Entender as roles](o-que-sao-roles.md).
* O jeito mais rápido é partir de uma role pronta e ajustar.

## Passo a passo

{% stepper %}
{% step %}
### Abra as roles

Dentro de qualquer módulo, clique em **Configurações › Roles & Permissões**. Clique em **Nova Role**. Abre a janela **Criar Nova Role**.

<figure><img src="../../.gitbook/assets/usuarios-criar-role-01.png" alt="Tela de roles com o botão Nova Role"><figcaption><p>Botão Nova Role</p></figcaption></figure>
{% endstep %}

{% step %}
### Dê nome e descrição

Preencha o nome e a descrição. Se quiser exigir o código no login de quem tiver essa role, ligue **MFA obrigatório**.

<figure><img src="../../.gitbook/assets/usuarios-criar-role-02.png" alt="Formulário Nova Role com nome, descrição e a chave MFA obrigatório"><figcaption><p>Nome, descrição e MFA obrigatório</p></figcaption></figure>
{% endstep %}

{% step %}
### Copie as permissões de outra role

Clique em **De outra role**, escolha a role e marque **Adicionar às atuais**. Clique em **Aplicar**.

<figure><img src="../../.gitbook/assets/usuarios-criar-role-03.png" alt="Janela De outra role com as opções Substituir tudo e Adicionar às atuais"><figcaption><p>Copiar de outra role</p></figcaption></figure>
{% endstep %}

{% step %}
### Ajuste e salve

Use **Buscar permissões...** para achar o que quer ligar ou desligar. Confira o **Resumo** e clique em **Criar Role**. Aparece **Role criada com sucesso!**.

<figure><img src="../../.gitbook/assets/usuarios-criar-role-04.png" alt="Lista de permissões filtrada pela busca e o Resumo da role"><figcaption><p>Permissões e Resumo</p></figcaption></figure>
{% endstep %}
{% endstepper %}

Depois, [atribua a role](atribuir-role.md) aos usuários.

## Dúvidas comuns

<details>

<summary>Qual a diferença entre Substituir tudo e Adicionar às atuais?</summary>

**Substituir tudo** apaga o que você já marcou e usa só as permissões da outra role. **Adicionar às atuais** soma as duas.

</details>

<details>

<summary>Para que serve o Colar?</summary>

Na lista de roles, clique no ícone **Copiar permissões** da role. Depois, na **Nova Role** ou no detalhe de outra role, clique em **Colar**. Funciona também entre abas do navegador e entre empresas.

</details>

<details>

<summary>Como excluo uma role?</summary>

Só as roles com o selo **Customizada** podem ser excluídas. O sistema pergunta: "Tem certeza que deseja excluir esta role? Esta ação não pode ser desfeita.".

</details>
