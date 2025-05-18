# Editar Setor

Esta página explica como modificar as informações de um setor existente no Sistema GNRX Gestão de EPI.

## Visão Geral

A edição de setores permite atualizar informações cadastrais e descrições para manter a estrutura organizacional sempre atualizada no sistema.

## Acessando a Tela de Edição

Existem duas formas de acessar a edição de um setor:

### Opção 1: A partir da Lista de Setores

1. No menu lateral, clique em **Estruturas**
2. Selecione **Setores**
3. Na lista de setores, localize o setor desejado
4. Clique no ícone de **Editar** (símbolo de lápis) na coluna de ações

![Editar via Lista](../../../assets/images/editar-setor-lista.png)

### Opção 2: A partir da Tela de Detalhes

1. Acesse a tela de detalhes do setor (clicando em seu nome na lista)
2. Clique no botão **Atualizar** no canto superior direito da tela

![Botão Atualizar](../../../assets/images/botao-atualizar-setor.png)

## Interface de Edição

A tela de edição apresenta um modal com o formulário preenchido com os dados atuais do setor:

![Formulário de Edição](../../../assets/images/formulario-editar-setor.png)

### Campos Editáveis

| Campo | Descrição | Considerações ao Editar |
|-------|-----------|-------------------------|
| **Nome** | Nome do setor | A alteração afetará todas as referências ao setor no sistema |
| **Descrição** | Informações adicionais | Campo opcional, pode ser usado para detalhar a função do setor |

## Processo de Edição

1. Modifique os campos necessários
2. Verifique cuidadosamente as alterações, especialmente no nome do setor
3. Clique no botão **Salvar** para confirmar as modificações
4. O sistema exibirá uma mensagem de confirmação após a atualização bem-sucedida

![Confirmação de Atualização](../../../assets/images/confirmacao-atualizacao-setor.png)

## Impacto das Alterações

A edição de um setor pode ter os seguintes impactos no sistema:

- Alterações no nome afetam todos os relatórios e listagens
- Modificações são refletidas em todas as unidades onde o setor está presente
- As atualizações são imediatamente visíveis para todos os usuários do sistema
- Histórico de entregas de EPIs mantém a associação com o setor, mesmo após a edição

## Limitações e Restrições

Algumas limitações se aplicam à edição de setores:

- Não é possível alterar o ID do setor
- Se o setor possui colaboradores vinculados, a alteração de nome pode gerar confusão
- Não é possível mesclar dois setores através da edição - para isso, crie um novo setor e reatribua os colaboradores

## Vinculação a Unidades

A edição do setor não afeta suas vinculações com unidades. Para gerenciar essas associações:

1. Após salvar as alterações de nome ou descrição, vá para a aba **Unidades**
2. Verifique as unidades atualmente vinculadas
3. Adicione ou remova unidades conforme necessário

![Unidades do Setor](../../../assets/images/unidades-setor.png)

## Visibilidade das Alterações

Após editar um setor:

- O novo nome é imediatamente exibido em todas as listas e relatórios
- Os colaboradores vinculados permanecem associados ao setor
- Os GHEs relacionados mantêm sua configuração
- O histórico de modificações é registrado para auditoria

## Melhores Práticas

Para uma edição eficiente de setores:

- Mantenha a consistência na nomenclatura, mesmo após alterações
- Comunique mudanças significativas aos usuários do sistema
- Documente o motivo das alterações importantes
- Evite mudanças frequentes na estrutura organizacional para não confundir os usuários
- Considere o impacto das alterações nos relatórios históricos

## Casos de Uso Comuns

Situações típicas para edição de setores incluem:

- Correção de erros ortográficos ou formatação
- Atualização para refletir mudanças na estrutura organizacional
- Melhoria na descrição para incluir informações mais detalhadas
- Padronização de nomenclatura em toda a empresa

## Próximos Passos

Após editar um setor, considere:

- Verificar se a edição está refletida corretamente nas diferentes unidades
- Revisar os [colaboradores vinculados](../colaboradores/listar-colaboradores.md) ao setor
- Atualizar os [GHEs](../ghe/README.md) relacionados, se necessário
- Informar as equipes de gestão sobre as mudanças realizadas

---

*Última atualização: 16 de Maio de 2025*