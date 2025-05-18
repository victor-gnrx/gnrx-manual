# Riscos Ocupacionais

Esta seção explica como gerenciar o catálogo de riscos ocupacionais no Sistema GNRX, permitindo associá-los aos Grupos Homogêneos de Exposição (GHEs) e, consequentemente, determinar os EPIs necessários para cada função.

## Visão Geral

Os riscos ocupacionais são os elementos presentes nos ambientes de trabalho que podem causar danos à saúde dos trabalhadores. No Sistema GNRX, o cadastro adequado destes riscos é fundamental para:

- Associação correta entre riscos e EPIs necessários
- Determinação automática dos equipamentos para cada GHE
- Documentação de conformidade com requisitos legais
- Emissão de relatórios precisos de análise de riscos

## Catálogo Padrão NR-6

O Sistema GNRX é fornecido com um catálogo completo de riscos baseado na Norma Regulamentadora 6 (NR-6), que classifica os riscos em cinco categorias principais:

1. **Riscos Físicos**: Ruído, vibrações, temperaturas extremas, radiações, pressões anormais, etc.
2. **Riscos Químicos**: Poeiras, fumos, névoas, neblinas, gases, vapores, substâncias químicas, etc.
3. **Riscos Biológicos**: Vírus, bactérias, fungos, parasitas, protozoários, etc.
4. **Riscos Ergonômicos**: Esforço físico intenso, levantamento de peso, postura inadequada, etc.
5. **Riscos de Acidentes**: Arranjo físico inadequado, máquinas sem proteção, ferramentas defeituosas, etc.

![Categorias de Riscos](../../../assets/images/categorias-riscos.png)

## Acessando o Catálogo de Riscos

1. No menu lateral, acesse **Configurações Gerais**
2. Selecione **Riscos**
3. O sistema exibirá o catálogo completo de riscos disponíveis

![Acesso ao Catálogo de Riscos](../../../assets/images/acesso-catalogo-riscos.png)

## Gerenciando Riscos Ocupacionais

### Visualizando o Catálogo

O catálogo de riscos é apresentado em uma lista organizada por categoria, com recursos de:

- Filtro por categoria de risco
- Pesquisa por nome ou descrição
- Visualização de riscos personalizados
- Indicação de riscos associados a GHEs

### Adicionando um Novo Risco

![Adicionar Novo Risco](../../../assets/images/adicionar-risco.png)

1. Clique no botão **Adicionar Risco**
2. Preencha o formulário com:
   - **Nome**: Identificação concisa do risco (ex: "Exposição a Vapores de Solventes")
   - **Categoria**: Selecione a categoria adequada (Físico, Químico, Biológico, etc.)
   - **Descrição**: Detalhamento do risco e seus potenciais efeitos à saúde
   - **EPIs Recomendados**: Seleção dos EPIs indicados para proteção contra este risco
3. Clique em **Salvar**

### Editando um Risco Existente

> **Nota:** Só é possível editar riscos personalizados. Os riscos padrão da NR-6 não podem ser modificados.

1. Localize o risco desejado na lista
2. Clique no ícone de **Editar**
3. Faça as alterações necessárias
4. Clique em **Salvar**

### Desativando um Risco

1. Localize o risco desejado na lista
2. Clique no ícone de **Desativar**
3. Confirme a desativação

> **Importante:** Desativar um risco não o remove dos GHEs já configurados, mas impede que seja selecionado em novos cadastros.

## Associação de Riscos a EPIs

Cada risco ocupacional deve estar associado aos EPIs adequados para proteção. Esta relação pode ser configurada:

1. Durante o cadastro/edição do próprio risco
2. Na configuração de um GHE específico
3. Através da matriz de riscos x EPIs

### Matriz de Riscos x EPIs

![Matriz de Riscos x EPIs](../../../assets/images/matriz-riscos-epis.png)

Esta funcionalidade permite uma visão consolidada e edição em massa:

1. No catálogo de riscos, clique no botão **Matriz de Riscos x EPIs**
2. O sistema exibirá uma matriz onde as linhas são os riscos e as colunas são os EPIs
3. Marque as células correspondentes às associações corretas
4. Clique em **Salvar Alterações**

## Considerações Importantes

### Customização para Setores Específicos

Embora o sistema venha com um catálogo completo, considere adicionar riscos específicos para seu setor de atuação, especialmente:

- Indústrias com processos químicos específicos
- Ambientes hospitalares com riscos biológicos particulares
- Construção civil com riscos ergonômicos e de acidentes característicos
- Atividades rurais com exposições específicas a agentes químicos ou biológicos

### Atualização Periódica

É recomendável revisar periodicamente o catálogo de riscos para:

- Incluir novos riscos identificados em avaliações ambientais
- Atualizar associações com EPIs conforme novas tecnologias de proteção
- Refinar descrições baseadas em novos conhecimentos técnicos

## Integração com o PPRA/PGR

O catálogo de riscos do Sistema GNRX deve estar alinhado com:

- PPRA (Programa de Prevenção de Riscos Ambientais)
- PGR (Programa de Gerenciamento de Riscos)
- Laudo LTCAT (Laudo Técnico de Condições Ambientais do Trabalho)
- Outros documentos técnicos de avaliação de riscos da empresa

Esta integração garante consistência na gestão de segurança e facilita auditorias e fiscalizações.