# Navegação e Uso do Catálogo de EPIs

## Introdução

O Catálogo de EPIs é uma biblioteca completa de todos os Equipamentos de Proteção Individual disponíveis no sistema GNRX. Esta funcionalidade permite visualizar, filtrar e gerenciar os EPIs conforme a classificação da NR-6, além de incluir equipamentos personalizados específicos da empresa.

![Interface do Catálogo de EPIs](../../../assets/images/catalogo-epis.png)

## Como Acessar

Para acessar o catálogo de EPIs:

1. Clique no menu **Configurações** na barra de navegação principal
2. Selecione a opção **EPIs** no submenu que se abre
3. A interface do catálogo será exibida, mostrando todas as categorias disponíveis

## Elementos da Interface

A tela do catálogo de EPIs apresenta os seguintes elementos:

### Cabeçalho

- **Título "EPIs"**: Indica a seção atual do sistema
- **Campo de busca**: Permite pesquisar EPIs específicos por nome ou código
- **Botão "Criar Novo EPI"**: Abre o formulário para adicionar um novo equipamento personalizado

### Filtros e Opções de Visualização

- **Filtro de categorias**: Permite selecionar uma ou mais categorias específicas
- **Checkbox "Exibir apenas EPIs"**: Mostra somente os EPIs padrão da base do sistema
- **Checkbox "Exibir apenas Customizados"**: Mostra somente os EPIs personalizados da empresa

### Estrutura Hierárquica

O catálogo é organizado em uma estrutura de árvore expansível com três níveis:

1. **Categorias**: Agrupamentos principais conforme a NR-6 (ex: EPI PARA PROTEÇÃO AUDITIVA)
2. **Tipos**: Subgrupos dentro de cada categoria (ex: Protetor auditivo)
3. **EPIs específicos**: Itens individuais com descrições detalhadas (ex: protetor auditivo circum-auricular)

## Navegação no Catálogo

### Expandir e Colapsar Categorias

- Clique na seta ▶ ao lado de uma categoria para expandir e mostrar os tipos contidos nela
- Clique na seta ▼ de uma categoria expandida para colapsá-la novamente
- O mesmo princípio se aplica para expandir e colapsar os tipos de EPIs

### Buscar EPIs Específicos

Para localizar rapidamente um EPI no catálogo:

1. Digite termos relevantes no campo "Buscar EPIs..." no topo da tela
2. O sistema filtrará automaticamente, mostrando apenas os itens que correspondem à busca
3. Os resultados manterão a estrutura hierárquica, destacando onde os itens encontrados estão localizados

A busca abrange:
- Nome do EPI
- Código de identificação
- Descrição detalhada

### Filtrar por Categoria

Para visualizar EPIs de categorias específicas:

1. Clique no seletor "Todas as categorias"
2. Escolha uma ou mais categorias de interesse
3. A visualização será atualizada para mostrar apenas as categorias selecionadas

### Filtrar por Origem

Para visualizar apenas determinados tipos de EPIs:

- Marque a opção "Exibir apenas EPIs" para ver somente os equipamentos padrão da NR-6
- Marque a opção "Exibir apenas Customizados" para ver somente os EPIs personalizados da empresa
- Deixe ambas as opções desmarcadas para ver todos os EPIs disponíveis

## Identificação e Codificação

Cada EPI no catálogo possui um código único que segue o padrão:

- **(EPI_X_NNN)** para tipos de EPIs
  - X: Letra da categoria (A a I)
  - NNN: Número sequencial do tipo

- **(EPI_X_NNN_y)** para EPIs específicos
  - X: Letra da categoria
  - NNN: Número sequencial do tipo
  - y: Letra minúscula para diferenciar EPIs do mesmo tipo

Exemplos:
- (EPI_C_001): Código para o tipo "Protetor auditivo"
- (EPI_C_001_a): Código para "protetor auditivo circum-auricular"

## Ações Disponíveis

Dependendo do tipo de EPI e do nível de permissão do usuário, as seguintes ações podem estar disponíveis:

- **Adicionar novo EPI**: Através do botão "Criar Novo EPI" no topo da tela
- **Editar**: Disponível apenas para EPIs personalizados da empresa
- **Inativar**: Disponível apenas para EPIs personalizados da empresa

## Considerações Importantes

- **EPIs da NR-6**: Os equipamentos da base pré-configurada não podem ser editados ou inativados
- **Organização**: A estrutura hierárquica segue o padrão oficial da NR-6 para facilitar localização
- **Referência cruzada**: Os EPIs do catálogo são os mesmos disponíveis para seleção em GHEs e riscos
- **Atualização**: O catálogo base é atualizado pelo sistema conforme mudanças na legislação

## Próximos Passos

A partir do catálogo de EPIs, você pode:

- [Adicionar EPI ao Catálogo](./adicionar-epi-catalogo.md) - Criar um novo EPI personalizado
- [Editar EPI do Catálogo](./editar-epi-catalogo.md) - Modificar um EPI personalizado existente
- Associar EPIs a riscos específicos no módulo de configuração de riscos
- Vincular EPIs a GHEs na configuração de Grupos Homogêneos de Exposição

---

*Última atualização: 18 de Maio de 2025*