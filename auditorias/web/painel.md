---
description: "Veja a conformidade, as não conformidades em aberto e as ações atrasadas."
icon: chart-pie
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

# Ver o painel de auditorias

**Para que serve:** ver de relance a conformidade das auditorias, o que está em aberto e onde agir. Ex.: descobrir qual unidade tem mais não conformidades no mês.

{% hint style="info" %}
**Quem pode fazer:** Supervisor, Gestor ou Administrador, com a permissão de ver o painel de auditorias.
{% endhint %}

## Antes de começar

* Tenha auditorias feitas no período. Veja [Criar uma auditoria](criar-auditoria.md).

## Passo a passo

{% stepper %}
{% step %}
### Abra o painel

Clique em **Painel de Auditorias**. Na primeira vez abre um tour com o que mudou: clique em **Ver o painel** ou em **Agora não**.

<figure><img src="../.gitbook/assets/aud-painel-01.png" alt="Painel de Auditoria com os filtros, o resumo do período e as abas Unidades, Setores, Usuários, Multas e Modelos"><figcaption><p>Painel de Auditoria</p></figcaption></figure>
{% endstep %}

{% step %}
### Ajuste os filtros

Escolha o período (vem no mês atual), as unidades, o modelo e a categoria. Os filtros valem para o painel inteiro. **Limpar** volta ao padrão.
{% endstep %}

{% step %}
### Leia o resumo

O topo mostra o percentual de conformidade e quantos itens foram conformes. Se houver ação atrasada ou pendente, use os atalhos para abrir as ações em **Planos de Ação**.
{% endstep %}

{% step %}
### Escolha a aba

| Aba | O que mostra |
| --- | --- |
| **Unidades** | Itens conformes, resolvidos e em aberto de cada unidade. |
| **Setores** | Os setores dentro de cada unidade, os que pedem mais atenção primeiro. |
| **Usuários** | Volume, qualidade e tempo de cada auditor. |
| **Multas** | A exposição a multas em aberto e a multa já evitada. |
| **Modelos** | Os modelos com mais não conformidades e os itens que mais falham. |
{% endstep %}
{% endstepper %}

## Deu errado?

{% hint style="warning" %}
**"Não foi possível carregar o dashboard"**: clique em **Tentar novamente**.
{% endhint %}

## Dúvidas comuns

<details>

<summary>Aparece "Nenhuma auditoria no período"?</summary>

Não há auditoria no período ou nos filtros escolhidos. Aumente o período ou clique em **Limpar**.

</details>

<details>

<summary>Por que o filtro de unidades está travado?</summary>

Você só tem uma unidade vinculada. O painel mostra apenas as unidades vinculadas ao seu usuário.

</details>

<details>

<summary>Como a multa é calculada?</summary>

Multa unitária × ocorrências. A multa unitária vem do valor informado no item ou, sem ele, do máximo da NR-28.

</details>

<details>

<summary>O que é a linha "Sem setor"?</summary>

As auditorias criadas sem setor. Elas entram na conta para o painel bater com os relatórios.

</details>
