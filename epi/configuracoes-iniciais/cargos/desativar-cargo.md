# Desativar Cargo

Esta página explica como desativar um cargo existente no Sistema GNRX Gestão de EPI, bem como as implicações desta ação.

## Visão Geral

A desativação de cargos é utilizada quando uma função específica deixa de existir na estrutura organizacional ou quando houve erro no cadastro. Diferente da exclusão definitiva, a desativação preserva o histórico para fins de auditoria e rastreabilidade.

## Quando Desativar um Cargo

As situações mais comuns para desativação incluem:

- Extinção da função na estrutura organizacional
- Reorganização de cargos e funções
- Correção de duplicidade (múltiplos cargos para a mesma função)
- Substituição por nova nomenclatura
- Cargos criados erroneamente

## Acessando a Função de Desativação

Para desativar um cargo:

1. No menu lateral, clique em **Estruturas**
2. Selecione **Cargos**
3. Na lista de cargos, localize o cargo desejado
4. Clique no ícone de **Excluir/Desativar** (símbolo de lixeira) na coluna de ações

![Desativar Cargo](../../../assets/images/desativar-cargo.png)

## Processo de Desativação

Ao iniciar a desativação, o sistema apresentará um diálogo de confirmação:

![Diálogo de Confirmação](../../../assets/images/dialogo-confirmacao-desativacao-cargo.png)

O diálogo inclui:

1. Alerta sobre as consequências da desativação
2. Informações sobre colaboradores associados ao cargo
3. Campo para informar o motivo da desativação (opcional, mas recomendado)
4. Botões de "Cancelar" e "Confirmar Desativação"

Para prosseguir:
1. Preencha o motivo da desativação (recomendado para fins de auditoria)
2. Clique em **Confirmar Desativação**
3. O sistema processará a solicitação e exibirá uma mensagem de confirmação

## Impacto da Desativação

Quando um cargo é desativado:

### O que acontece:
- O cargo recebe o status "Inativo" na lista de cargos
- Ele deixa de aparecer em listas de seleção para novos colaboradores
- Relatórios padrão filtram o cargo, a menos que explicitamente incluído
- O histórico completo permanece acessível para consulta

### O que NÃO acontece:
- O registro do cargo não é excluído do banco de dados
- Históricos de entregas de EPIs associados ao cargo não são removidos
- Colaboradores já vinculados ao cargo não são removidos automaticamente
- Documentos e registros legais permanecem intactos

## Verificações Prévias à Desativação

Antes de desativar um cargo, o sistema verifica:

| Item | Verificação | Ação Recomendada |
|------|-------------|------------------|
| **Colaboradores Ativos** | Se há funcionários ativos associados ao cargo | Transferir para outros cargos ativos |
| **Histórico Recente** | Atividades recentes relacionadas ao cargo | Documentar o motivo da desativação |

## Reativando um Cargo

Para reativar um cargo previamente desativado:

1. Na lista de cargos, marque a opção **Mostrar Inativos**
2. Localize o cargo desativado (indicado com status "Inativo")
3. Clique no ícone de **Reativar** (símbolo de reciclagem)
4. Confirme a reativação no diálogo exibido

![Reativar Cargo](../../../assets/images/reativar-cargo.png)

## Considerações Importantes

- A desativação deve ser preferida à exclusão quando o cargo já possui histórico
- Considere a reatribuição de colaboradores antes da desativação
- Documente adequadamente o motivo da desativação para referência futura
- Verifique o impacto em relatórios históricos antes de proceder
- Consulte o setor de RH antes de desativar cargos com muitos colaboradores associados

## Alternativas à Desativação

Em alguns casos, existem alternativas preferíveis à desativação:

- **Renomeação**: Se apenas o nome mudou, edite o cargo em vez de desativá-lo
- **Reorganização**: Se houve fusão de funções, considere manter um dos cargos e transferir os colaboradores
- **Atualização de Descrição**: Se a função mudou ligeiramente, considere apenas documentar as novas responsabilidades

## Impacto em Relatórios

A desativação de cargos pode afetar a análise de dados históricos:

- Relatórios que incluem períodos anteriores à desativação ainda mostrarão o cargo
- Análises comparativas entre períodos podem precisar considerar a desativação
- Estatísticas de uso de EPIs por cargo continuarão incluindo o histórico do cargo desativado

## Logs e Auditoria

O sistema mantém registros detalhados das desativações:

- Data e hora da desativação
- Usuário que executou a ação
- Motivo informado
- Estado dos vínculos no momento da desativação

Estes logs estão disponíveis para administradores do sistema na seção de Auditoria.

## Melhores Práticas

- Planeje a desativação de cargos como parte de uma revisão estruturada da organização
- Comunique mudanças aos colaboradores afetados
- Atualize documentação relacionada (organogramas, descrições de cargo)
- Mantenha um registro das razões para desativação para referência futura
- Coordene a desativação com outros departamentos, como RH e Segurança do Trabalho

---

*Última atualização: 16 de Maio de 2025*