---
description: Publique um curso EAD no portal do aluno.
icon: upload
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

# Publicar um curso no portal

**Para que serve:** colocar um curso EAD no portal, com capa, descrição, carga horária e o instrutor que assina o certificado.

{% hint style="info" %}
**Quem pode fazer:** Supervisor, Gestor ou Administrador, com a permissão de gerenciar o conteúdo do EAD.
{% endhint %}

## Antes de começar

* [Monte o conteúdo do curso](montar-curso-ead.md).
* Cadastre a [assinatura do instrutor](../estruturas/instrutores/editar-instrutor.md). Ele assina o certificado.

## Passo a passo

{% stepper %}
{% step %}
### Abra o curso

Clique em **Turmas › Portal do aluno**, aba **Cursos**. Aparecem os treinamentos com módulos EAD. Clique na capa do curso.

<figure><img src="../.gitbook/assets/portal-cursos-01.png" alt="Aba Cursos com as capas dos treinamentos que têm EAD"><figcaption><p>Aba Cursos</p></figcaption></figure>
{% endstep %}

{% step %}
### Preencha e publique

Escolha o **Instrutor responsável** (obrigatório para publicar). Confira a **Carga horária**, escreva a descrição e envie a **Capa retrato** e a **Capa paisagem**. Ligue **Publicado no portal**. Clique em **Salvar curso**. Aparece "Curso salvo.".

<figure><img src="../.gitbook/assets/portal-cursos-02.png" alt="Janela do curso com Instrutor responsável, Carga horária, capas e a chave Publicado no portal"><figcaption><p>Dados do curso</p></figcaption></figure>
{% endstep %}
{% endstepper %}

Depois, [libere os acessos](liberar-acessos.md).

## Deu errado?

| Mensagem na tela | O que fazer |
| --- | --- |
| "Ainda não tem módulo disponível. Envie os vídeos na aba EAD do treinamento." | [Monte o conteúdo](montar-curso-ead.md). |
| "Falta o conteúdo programático do treinamento no catálogo: ele vai no certificado." | Clique em **Cadastrar o conteúdo programático**. |
| "Tem parte prática: não conclui só a distância. Programe uma turma semipresencial." | [Programe uma turma](../turmas/programar-treinamento.md) semipresencial. |
| "Este instrutor foi inativado. Escolha outro." | Escolha outro instrutor ativo. |
| "Instrutor sem assinatura" | Cadastre a [assinatura do instrutor](../estruturas/instrutores/editar-instrutor.md). |

## Dúvidas comuns

<details>

<summary>Quem vê o curso publicado?</summary>

Quem tem acesso pelas regras da aba **Acessos**.

</details>

<details>

<summary>A carga horária já vem preenchida?</summary>

Vem sugerida: a gravada, a mínima do catálogo ou a soma dos vídeos.

</details>
