---
description: Como criar e gerenciar modelos de checklist personalizados para suas necessidades específicas
icon: edit
---

# Modelos Customizados

Os Modelos Customizados permitem criar checklists totalmente personalizados, adaptados às necessidades específicas da sua empresa, processos internos ou requisitos particulares do seu negócio.

![Editor de Modelos Customizados](/images/editor-modelos-customizados.png)

## Vantagens dos Modelos Customizados

- **Flexibilidade total** na criação da estrutura
- **Múltiplos tipos de resposta** para diferentes necessidades
- **Hierarquia personalizada** de seções e itens
- **Adaptação completa** ao seu negócio e processos

## Criando um Novo Modelo Customizado

1. No menu lateral, acesse **"Modelos Customizados"**
2. Clique no botão **"Novo Modelo"**
3. Preencha as informações básicas:
   - Nome do modelo
   - Descrição (opcional)
   - Tipo (Auditoria, Inspeção, Verificação)
4. Configure as opções gerais:
   - Permitir fotos
   - Permitir observações
   - Sistema de pontuação (se aplicável)
5. Clique em **"Criar Modelo"**

## Estruturando seu Modelo

### Adicionando Seções

As seções são agrupamentos de itens que organizam seu checklist:

1. Clique em **"Adicionar Seção"**
2. Defina:
   - Código (ex: A, B, C ou 1, 2, 3)
   - Nome da seção
   - Descrição (opcional)
3. Defina a ordem da seção
4. Para criar subseções, use o botão **"Adicionar Subseção"** dentro de uma seção existente

![Adicionando Seções](/images/adicionar-secoes.png)

### Adicionando Itens

Os itens são as perguntas ou verificações do seu checklist:

1. Dentro de uma seção, clique em **"Adicionar Item"**
2. Configure:
   - Código do item (ex: 1.1, 1.2, A.1)
   - Nome/pergunta
   - Descrição detalhada (opcional)
   - Tipo de item (veja abaixo)
   - Obrigatoriedade
   - Ação corretiva sugerida (opcional)

![Adicionando Itens](/images/adicionar-itens.png)

## Tipos de Itens Disponíveis

O sistema oferece diversos tipos de itens para compor seu modelo:

| Tipo de Item | Descrição | Uso Recomendado |
|--------------|-----------|-----------------|
| Conformidade | Conforme/Não Conforme/NA | Verificações de padrões |
| Escala | Pontuação de 1-5 ou 1-10 | Avaliações de qualidade |
| Texto | Campo de texto livre | Comentários e observações |
| Número | Valor numérico | Medições e contagens |
| Data | Seletor de data | Verificação de validades |
| Hora | Seletor de hora | Registro de horários |
| Informativo | Apenas exibe informação | Instruções e orientações |

## Criando o Cabeçalho

O cabeçalho define as informações que serão coletadas no início de cada auditoria:

1. Na aba **"Cabeçalho"**, clique em **"Adicionar Campo"**
2. Configure cada campo:
   - Chave (nome do campo)
   - Tipo de dado (texto, número, data, etc)
   - Obrigatoriedade
   - Valor padrão (opcional)
   - Descrição de ajuda (opcional)

![Configuração de Cabeçalho](/images/configuracao-cabecalho.png)

## Configurações Avançadas

### Sistema de Pontuação

Para modelos que utilizam avaliação por pontos:

1. Acesse a aba **"Pontuação"**
2. Configure:
   - Escala (1-5, 1-10, personalizada)
   - Peso para cada seção (opcional)
   - Método de cálculo (média simples, ponderada)
   - Níveis de classificação do resultado final

### Regras de Criticidade

Defina a classificação de não conformidades:

1. Acesse a aba **"Criticidade"**
2. Configure os níveis (Alta, Média, Baixa)
3. Defina critérios para classificação automática

## Versionamento de Modelos

O sistema mantém controle de versões dos modelos customizados:

- Cada alteração gera uma nova versão
- Auditorias já realizadas mantêm a versão original
- Histórico completo de mudanças por versão

## Duplicação e Importação

Para acelerar a criação de novos modelos:

- Use **"Duplicar"** para criar uma cópia editável de um modelo existente
- A função **"Importar"** permite trazer modelos de outras unidades ou de biblioteca padrão

## Dicas de Utilização

- 💡 **Dica 1**: Inicie com modelos mais simples e adicione complexidade conforme necessário
- 💡 **Dica 2**: Padronize a codificação de seções e itens para facilitar referências
- 💡 **Dica 3**: Teste seu modelo com uma auditoria piloto antes do uso em larga escala

## Próximos Passos

- [Criar uma auditoria com modelo customizado](/auditorias/web/nova-auditoria.md)
- [Analisar resultados de auditorias](/auditorias/web/visualizar-auditorias.md)
- [Gerar relatórios personalizados](/auditorias/web/visualizar-relatorios.md)