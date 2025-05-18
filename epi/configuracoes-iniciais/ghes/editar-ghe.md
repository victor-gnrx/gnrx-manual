# Editar GHE

Esta página explica como modificar as informações de um Grupo Homogêneo de Exposição (GHE) existente no Sistema GNRX Gestão de EPI.

## Visão Geral

A edição de GHEs permite atualizar informações cadastrais, descrições e, mais importante, os riscos e EPIs associados ao grupo, mantendo a gestão de segurança sempre atualizada.

## Acessando a Tela de Edição

Existem duas formas de acessar a edição de um GHE:

### Opção 1: A partir da Lista de GHEs

1. No menu lateral, clique em **Estruturas**
2. Selecione **GHEs**
3. Na lista de GHEs, localize o grupo desejado
4. Clique no ícone de **Editar** (símbolo de lápis) na coluna de ações

![Editar via Lista](../../../assets/images/editar-ghe-lista.png)

### Opção 2: A partir da Tela de Detalhes

1. Acesse a tela de detalhes do GHE (clicando em seu nome na lista)
2. Clique no botão **Atualizar** no canto superior direito da tela

![Botão Atualizar](../../../assets/images/botao-atualizar-ghe.png)

## Edição de Informações Básicas

A tela de edição apresenta o formulário preenchido com os dados atuais do GHE:

![Formulário de Edição](../../../assets/images/formulario-editar-ghe.png)

### Campos Editáveis

| Campo | Descrição | Considerações ao Editar |
|-------|-----------|-------------------------|
| **Nome** | Identificação do GHE | A alteração afetará todas as referências ao grupo no sistema |
| **Unidade** | Unidade física vinculada | Não pode ser alterada após a criação |
| **Descrição** | Detalhamento do grupo | Campo opcional para informações complementares |
| **Medidas de Controle** | Controles implementados | Descreva medidas administrativas, de engenharia ou EPCs |

## Processo de Edição de Dados Básicos

1. Modifique os campos necessários
2. Verifique cuidadosamente as alterações
3. Clique no botão **Salvar** para confirmar as modificações
4. O sistema exibirá uma mensagem de confirmação após a atualização bem-sucedida

## Edição de Riscos e EPIs

A parte mais importante da edição de um GHE é a gestão dos riscos associados e seus EPIs correspondentes:

### Acessando a Edição de Riscos

1. Na tela de detalhes do GHE, selecione a aba **Riscos / EPIs**
2. Clique no botão **Editar** para modificar os riscos associados

![Edição de Riscos](../../../assets/images/edicao-riscos-ghe.png)

### Interface de Seleção de Riscos

A tela de edição de riscos apresenta:

1. **Barra de Pesquisa**: Para localizar riscos específicos
2. **Filtro por Categoria**: Para visualizar riscos por tipo (físicos, químicos, etc.)
3. **Lista de Riscos**: Com caixas de seleção para cada risco
4. **Descrições**: Detalhamento de cada risco para facilitar a identificação

### Processo de Seleção de Riscos

1. Utilize os filtros para localizar os riscos relevantes
2. Marque as caixas de seleção para os riscos que se aplicam ao GHE
3. Você pode alternar entre **Mostrar Apenas Selecionados** e visualização completa
4. Após finalizar a seleção, clique em **Salvar** para confirmar as alterações

### Edição de EPIs Associados

Para cada risco selecionado, é possível gerenciar os EPIs correspondentes:

1. Clique no botão **Ver EPIs** ao lado de cada risco
2. O sistema exibirá a tela de seleção de EPIs para aquele risco específico
3. Navegue pelas categorias de EPIs (cabeça, auditiva, etc.)
4. Selecione ou desmarque os EPIs conforme necessário
5. Clique em **Salvar alterações** para confirmar

![Edição de EPIs](../../../assets/images/edicao-epis-risco.png)

## Impacto das Alterações

A edição de um GHE pode ter os seguintes impactos no sistema:

### Alterações de Dados Básicos
- Modificações no nome afetam relatórios e buscas
- Atualizações na descrição melhoram a documentação interna
- Alterações nas medidas de controle complementam a gestão de segurança

### Alterações de Riscos
- Adição de novos riscos pode gerar necessidade de EPIs adicionais
- Remoção de riscos pode tornar certos EPIs desnecessários
- Mudanças nos riscos devem refletir alterações reais nas condições de trabalho

### Alterações de EPIs
- Modificações afetam diretamente quais equipamentos serão fornecidos aos colaboradores
- Alterações em EPIs impactam solicitações futuras e verificações de conformidade
- As mudanças não afetam automaticamente entregas já realizadas

## Registro de Alterações

O sistema mantém um histórico das modificações realizadas:

- A coluna **Atualizado em** na lista de GHEs mostra a data da última alteração
- Logs detalhados são mantidos para fins de auditoria
- As modificações são imediatamente visíveis para todos os usuários do sistema

## Melhores Práticas

Para uma edição eficiente de GHEs:

- Documente o motivo das alterações significativas
- Realize modificações apenas com base em avaliações técnicas atualizadas
- Comunique mudanças relevantes aos responsáveis por segurança do trabalho
- Mantenha alinhamento com documentos oficiais (PGR/PPRA, PCMSO)
- Revise os EPIs associados sempre que alterar os riscos
- Verifique o impacto das alterações nos colaboradores vinculados ao GHE

## Limitações e Restrições

Algumas limitações se aplicam à edição de GHEs:

- Não é possível alterar a unidade vinculada ao GHE
- Se o GHE possui colaboradores associados, alterações nos riscos e EPIs devem ser cautelosas
- Riscos eliminados que já possuem histórico de proteção não são removidos dos registros anteriores

## Próximos Passos

Após editar um GHE, considere:

- Verificar a lista de [colaboradores vinculados](../colaboradores/README.md) para garantir a correta proteção
- Revisar [solicitações pendentes](../../solicitacoes/README.md) que possam ser afetadas pelas alterações
- Atualizar documentação relacionada para manter a consistência das informações

---

*Última atualização: 16 de Maio de 2025*