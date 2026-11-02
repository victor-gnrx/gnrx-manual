---
description: Decida se pendência documental avisa ou bloqueia entregas e treinamentos.
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

# Configurar o bloqueio documental

**Para que serve:** decidir o que acontece quando um colaborador está com documento pendente, vencido ou reprovado: nada, só um aviso, ou o bloqueio.

{% hint style="info" %}
**Quem pode fazer:** Gestor ou Administrador, com a permissão de editar alertas e política de bloqueio documental.
{% endhint %}

## Antes de começar

* Monte a [matriz de exigência](matriz-de-exigencia.md).

## Passo a passo

{% stepper %}
{% step %}
### Abra o bloqueio

Clique em **Configurações › Bloqueio**.

<figure><img src="../.gitbook/assets/docs-bloqueio-01.png" alt="Tela Bloqueio documental com os seletores de Entrega de itens e de Treinamento"><figcaption><p>Bloqueio documental</p></figcaption></figure>
{% endstep %}

{% step %}
### Escolha para cada situação

Em cada situação, escolha **Desligado**, **Só avisar** ou **Bloquear**:

* **Entrega de itens:** entrega de EPI, entrega direta, entrega de produto, entrega sem estoque e entrega pelo app.
* **Treinamento:** programar turma, adicionar participantes, adicionar sessão e registrar presença.

Clique em **Salvar alterações**. Aparece "Política de bloqueio salva.".
{% endstep %}
{% endstepper %}

## Deu errado?

| Mensagem na tela | O que fazer |
| --- | --- |
| "Documentação irregular impede receber itens: ... Regularize os documentos ou solicite uma liberação excepcional." | Regularize os documentos ou [peça uma liberação](../liberacoes/solicitar-liberacao.md). |
| "Documentação irregular impede participar do treinamento: ..." | Mesma coisa. |

## Dúvidas comuns

<details>

<summary>A pessoa precisa trabalhar com documento pendente.</summary>

Peça uma [liberação excepcional](../liberacoes/solicitar-liberacao.md).

</details>

<details>

<summary>Vale para quais módulos?</summary>

Para as entregas da Gestão de EPI e para as operações de Treinamentos.

</details>
