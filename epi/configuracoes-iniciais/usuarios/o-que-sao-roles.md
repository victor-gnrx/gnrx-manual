---
description: Saiba o que cada role pode fazer no GNRx.
icon: users-gear
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

# Entender as roles

**Para que serve:** saber o que cada role pode fazer, para escolher a certa para cada pessoa.

{% hint style="info" %}
**Quem pode fazer:** qualquer pessoa pode ler esta página. Para ver as roles no sistema, você precisa da permissão de ver roles (Administrador).
{% endhint %}

## Antes de começar

* Uma **role** é um pacote de permissões. Você dá uma role ao usuário e ele ganha tudo o que está nela.
* As roles ficam em **Configurações › Roles & Permissões** (no Treinamento, **Configurações › Roles e Permissões**), dentro de qualquer módulo.

<figure><img src="../../.gitbook/assets/usuarios-roles-01.png" alt="Tela de roles com a chave Incluir roles do sistema ligada, mostrando as roles do sistema com o selo Sistema"><figcaption><p>Tela de roles</p></figcaption></figure>

## Quem pode o quê

| Role | O que pode fazer |
| --- | --- |
| **Operador** | O dia a dia: faz auditoria, preenche formulário, pede EPI, registra ocorrência, vê o DDS e o próprio treinamento. |
| **Supervisor** | Tudo do Operador, mais: entrega e devolve EPI, aprova solicitações e compras, conduz o DDS, investiga ocorrências, conduz a eleição e as reuniões da CIPA, cuida de turmas e matrículas e vê os painéis. |
| **Gestor** | Quase tudo. **Não pode:** mexer em usuários e roles, criar ou inativar estruturas (unidade, setor, cargo, turno, terceiro) e colaboradores, gerenciar o estoque de EPI, mudar as configurações da empresa e o WhatsApp, ver as denúncias da CIPA e invalidar certificado. |
| **Administrador** | Tudo. |
| **Acesso Empresa (CNPJ)** | Tudo, sem depender de role. |

Quer a lista completa, permissão por permissão? Veja [Consultar as permissões](sistema-permissoes-roles.md).

{% hint style="info" %}
Quem não tem as permissões de ver "de todos" vê só o que criou ou o que foi atribuído a ele.
{% endhint %}

## Dúvidas comuns

<details>

<summary>Posso mudar as permissões do Operador?</summary>

Não. As 4 roles com o selo **Sistema** não podem ser editadas nem excluídas. Para ter uma versão própria, [crie uma role](criar-role.md) a partir dela.

</details>

<details>

<summary>O que é o selo Customizada?</summary>

É uma role criada pela sua empresa. Ela pode ser editada e excluída.

</details>

<details>

<summary>Dá para dar uma role só para um setor?</summary>

Não. Hoje, o que limita o que a pessoa vê são as [unidades vinculadas a ela](vincular-unidades.md).

</details>
