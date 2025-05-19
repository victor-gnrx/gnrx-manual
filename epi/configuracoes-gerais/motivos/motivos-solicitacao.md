# Gerenciamento de Motivos de Solicitação

## Introdução

Os Motivos de Solicitação são as justificativas utilizadas quando se solicita a entrega de Equipamentos de Proteção Individual (EPIs) para um colaborador. Esta funcionalidade permite padronizar as razões pelas quais novos EPIs são requisitados, facilitando o controle do fluxo de distribuição e a análise posterior dos padrões de solicitação.

![Interface de Motivos de Solicitação](../../../assets/images/motivos-solicitacao.png)

## Como Acessar

Para gerenciar os Motivos de Solicitação:

1. Acesse o menu **Configurações** na barra de navegação principal
2. Selecione a opção **Motivos** no submenu que se abre
3. Na interface de Gestão de Motivos, clique na aba **Solicitação**
4. A lista de Motivos de Solicitação será exibida automaticamente

## Elementos da Interface

A tela de Motivos de Solicitação apresenta os seguintes elementos:

### Cabeçalho

- **Título "Motivos de Solicitação"**: Indica a seção atual
- **Botão "Novo Motivo"**: Permite adicionar um novo motivo de solicitação
- **Campo de pesquisa**: Filtro para localizar motivos específicos

### Tabela de Motivos

A tabela principal exibe os motivos cadastrados com as seguintes colunas:

- **Motivo**: Nome descritivo da justificativa
- **Sigla**: Abreviação de até 4 caracteres para identificação rápida
- **Descrição**: Detalhamento adicional (quando disponível)
- **Situação**: Status do motivo (Ativo ou Inativo)
- **Ações**: Botões para gerenciar o motivo (inativar)

## Motivos Padrão

O sistema GNRX geralmente vem com alguns motivos de solicitação pré-configurados, como:

- **Primeira Solicitação (PS)**: Para colaboradores que estão recebendo o EPI pela primeira vez
- **Troca Recorrente (TR)**: Para substituição periódica conforme prazo de validade ou desgaste
- **Perda (PER)**: Para reposição de EPIs extraviados ou perdidos

## Funcionalidades Principais

### Visualização de Motivos

A lista exibe todos os motivos de solicitação configurados no sistema, incluindo:
- Motivos pré-configurados padrão
- Motivos personalizados adicionados pela empresa

### Pesquisa e Filtragem

Para localizar motivos específicos:
1. Digite termos relevantes no campo "Pesquisar motivos..."
2. A lista será filtrada automaticamente conforme você digita
3. A pesquisa abrange nome do motivo, sigla e descrição

### Ordenação

É possível ordenar a lista clicando nos cabeçalhos das colunas:
- Ordenação alfabética por motivo
- Ordenação por sigla
- Ordenação por situação

## Gerenciamento de Motivos

### Adicionar Novo Motivo

Para criar um motivo de solicitação personalizado:

1. Clique no botão **Novo Motivo** no canto superior direito
2. No modal que se abre, preencha os campos:
   - **Motivo**: Nome claro e descritivo da justificativa
   - **Sigla**: Abreviação de até 4 caracteres (preferencialmente maiúsculas)
   - **Descrição (opcional)**: Detalhamento adicional quando necessário
3. Clique em **Salvar** para confirmar a criação

### Inativar Motivo

Para inativar um motivo de solicitação:

1. Localize o motivo na lista
2. Clique no ícone de lixeira na coluna "Ações"
3. Confirme a inativação no modal de confirmação que se abre
4. O motivo será marcado como inativo e não aparecerá nas opções de seleção para novas solicitações

**Importante**: A inativação não exclui o motivo permanentemente, apenas impede seu uso em novas operações. Registros históricos que utilizaram este motivo permanecerão inalterados.

## Boas Práticas

Para um gerenciamento eficaz dos motivos de solicitação:

- **Seja claro e objetivo**: Use nomes descritivos que identifiquem facilmente o propósito
- **Evite duplicações**: Verifique se não existem motivos similares antes de criar novos
- **Padronize as siglas**: Mantenha um padrão consistente para facilitar a identificação
- **Limite a quantidade**: Mantenha apenas os motivos realmente necessários para evitar confusão
- **Revise periodicamente**: Avalie regularmente se todos os motivos continuam relevantes

## Aplicação Prática

Os motivos de solicitação são utilizados em:

- **Fluxo de solicitação de EPIs**: Seleção obrigatória ao criar uma nova solicitação
- **Relatórios gerenciais**: Análise de padrões de solicitação por motivo
- **Documentação**: Registro formal da justificativa para fornecimento de equipamentos
- **Auditoria**: Evidência para processos de fiscalização e certificação

## Considerações Importantes

- **Impacto nas análises**: A consistência no uso dos motivos afeta diretamente a qualidade dos relatórios
- **Adequação normativa**: Considere incluir motivos que facilitem a demonstração de conformidade com normas regulamentadoras
- **Evolução do processo**: Revise e adapte os motivos conforme a maturidade do processo de gestão de EPIs

## Próximos Passos

Após configurar os motivos de solicitação, você pode:

- Verificar sua aplicação no processo de [Criação de Solicitações](../../solicitacoes/nova-solicitacao.md)
- Configurar os [Motivos de Devolução](./motivos-devolucao.md) para completar o ciclo de gestão
- Analisar relatórios de distribuição de EPIs por motivo para identificar tendências

---

*Última atualização: 18 de Maio de 2025*