# Guia de escrita do manual GNRx

Padrão obrigatório para toda página nova ou revisada. O leitor é leigo e tem pressa: a página precisa ser rápida e visual.

## Regras

0. **Frontmatter.** Toda página começa com frontmatter que tem `icon:` (ícone do Font Awesome) e `description:` de uma linha. Use também o bloco `layout:` de `epi/painel.md`.
1. **Uma tarefa por página.** O título é uma ação: "Cadastrar um colaborador", e não "Colaboradores".
2. **Topo da página.** Comece com uma linha `**Para que serve:** ...`. Logo depois, coloque um `{% hint style="info" %}` com `**Quem pode fazer:** ...`:
   - cite a role pelo nome (Operador, Supervisor, Gestor ou Administrador);
   - escreva a permissão por extenso, como "permissão de criar usuários". Nunca use a chave crua.
3. **`## Antes de começar`.** Liste os pré-requisitos, cada um com link (ex.: "cadastre a [unidade](...) primeiro").
4. **Passo a passo em `{% stepper %}` / `{% step %}`.**
   - Cada passo é uma frase curta no imperativo.
   - Botões e menus vão em **negrito**.
   - Cada passo tem um print.
   - O caminho de menu usa "›": **Estruturas › Colaboradores**. Nunca use "→" nem "->".
5. **`## Deu errado?`** Mostre a mensagem real do sistema e o que fazer, dentro de `{% hint style="warning" %}`. Não invente mensagens e nunca use o título técnico do erro (ex.: "Bad Request").
   - Mais de 3 erros: troque os hints por uma tabela de duas colunas, "Mensagem na tela" e "O que fazer". Cada linha é uma mensagem e cada célula tem uma frase curta. Ordene do caso mais comum para o mais raro.
6. **`## Dúvidas comuns`.** De 2 a 4 perguntas curtas.
7. **Linguagem.**
   - Frases curtas, sempre "você", sem jargão.
   - A página deve caber em uma a duas telas.
   - Escreva sempre "GNRx".
8. **Imagens.**
   - O arquivo se chama `<modulo>-<tarefa>-<nn>.png` e fica em `.gitbook/assets/` do próprio módulo (de uma subpasta, `../.gitbook/assets/`).
   - Use `<figure><img src="..." alt="descrição real"><figcaption><p>o que o print mostra</p></figcaption></figure>`.
   - O `alt` é sempre preenchido.
   - É proibido usar nomes como `image (N).png`.
9. **Estrutura.**
   - Há uma pasta por módulo (`epi/`, `auditorias/`, `formularios/`...).
   - As páginas comuns (acesso, usuários, roles, unidades, setores, cargos, GHE e colaboradores) têm o original em `epi/`. Os outros módulos as incluem com `{% include "../../../epi/..." %}`, como em `auditorias/web/estrutura/sistema-permissoes-roles.md`.
   - A página de include tem **sempre** o mesmo nome de arquivo do original, para os links relativos funcionarem.
   - O include espelha a profundidade de pasta do original. `epi/` equivale a `auditorias/web/` e `formularios/sistema-web/`, e `epi/configuracoes-iniciais/<tema>/` equivale a `estrutura(s)/<tema>/`. Exemplo: `epi/configuracoes-iniciais/usuarios/criar-usuario.md` é incluído em `auditorias/web/estrutura/usuarios/criar-usuario.md`.
   - O `SUMMARY.md` de cada módulo segue a ordem do menu do app.
   - O `README.md` de cada módulo tem cards (`<table data-view="cards">`) em duas seções: "Comece por aqui" e "Tarefas do dia a dia".
10. **Fora do manual.** Não documente:
    - o Painel Admin GNRx;
    - o MCP;
    - endpoints internos.

    Não prometa "role por setor". Hoje, o que limita o que o usuário vê são as **unidades** vinculadas a ele.

## Modelo de página

```markdown
---
description: Registre uma pessoa para entregar EPIs a ela.
icon: user-plus
layout: ...  # mesmo bloco de epi/painel.md
---

# Cadastrar um colaborador

**Para que serve:** registrar uma pessoa para entregar EPIs a ela.

{% hint style="info" %}
**Quem pode fazer:** Gestor ou Administrador, com a permissão de criar colaboradores.
{% endhint %}

## Antes de começar

* Cadastre a [unidade](../unidades/criar-unidade.md) primeiro.

## Passo a passo

{% stepper %}
{% step %}
### Abra a tela de colaboradores

Clique em **Estruturas › Colaboradores**.

<figure><img src="../.gitbook/assets/epi-colaborador-01.png" alt="Menu Estruturas aberto com a opção Colaboradores destacada"><figcaption><p>Menu Estruturas</p></figcaption></figure>
{% endstep %}
{% endstepper %}

## Deu errado?

{% hint style="warning" %}
**"Mensagem real do sistema"**: o que fazer.
{% endhint %}

## Dúvidas comuns

<details>
<summary>Pergunta curta?</summary>

Resposta curta.

</details>
```
