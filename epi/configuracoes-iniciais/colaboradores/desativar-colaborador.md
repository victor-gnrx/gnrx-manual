# Desativar Colaborador

Esta página explica como desativar um colaborador existente no Sistema GNRX Gestão de EPI, bem como as implicações desta ação.

## Visão Geral

A desativação de colaboradores é utilizada quando um funcionário se desliga da empresa ou está temporariamente afastado. Diferente da exclusão definitiva, a desativação preserva todo o histórico para fins de auditoria e rastreabilidade.

## Quando Desativar um Colaborador

As situações mais comuns para desativação incluem:

- Desligamento do funcionário (demissão ou aposentadoria)
- Afastamento temporário prolongado
- Transferência para outra empresa do grupo
- Licenças extensas
- Correção de cadastros duplicados

## Acessando a Função de Desativação

Para desativar um colaborador:

1. No menu lateral, clique em **Estruturas**
2. Selecione **Colaboradores**
3. Na lista de colaboradores, localize o colaborador desejado
4. Clique no ícone de **Excluir/Desativar** (símbolo de lixeira) na coluna de ações

![Desativar Colaborador](../../../assets/images/desativar-colaborador.png)

## Processo de Desativação

Ao iniciar a desativação, o sistema apresentará um diálogo de confirmação:

![Diálogo de Confirmação](../../../assets/images/dialogo-confirmacao-desativacao-colaborador.png)

O diálogo inclui:

1. Alerta sobre as consequências da desativação
2. Informações sobre itens pendentes (EPIs não devolvidos)
3. Campo para informar o motivo da desativação (opcional, mas recomendado)
4. Campo para data de encerramento da atividade (opcional)
5. Botões de "Cancelar" e "Confirmar Desativação"

Para prosseguir:
1. Preencha o motivo da desativação (recomendado para fins de auditoria)
2. Informe a data de encerramento da atividade, se aplicável
3. Clique em **Confirmar Desativação**
4. O sistema processará a solicitação e exibirá uma mensagem de confirmação

## Impacto da Desativação

Quando um colaborador é desativado:

### O que acontece:
- O colaborador recebe o status "Inativo" na lista
- Ele deixa de aparecer em listas de seleção para novas solicitações
- Relatórios padrão filtram o colaborador, a menos que explicitamente incluído
- O histórico completo permanece acessível para consulta
- O acesso ao aplicativo móvel é automaticamente bloqueado

### O que NÃO acontece:
- O registro do colaborador não é excluído do banco de dados
- Históricos de entregas de EPIs não são removidos
- Obrigações de devolução de EPIs não são automaticamente canceladas
- EPIs associados não são automaticamente liberados do inventário

## Verificações Prévias à Desativação

Antes de desativar um colaborador, o sistema verifica:

| Item | Verificação | Ação Recomendada |
|------|-------------|------------------|
| **EPIs em Posse** | Se há equipamentos não devolvidos | Registrar devolução ou perda antes da desativação |
| **Solicitações Pendentes** | Se existem solicitações em andamento | Concluir ou cancelar solicitações |
| **Entregas Recentes** | EPIs entregues recentemente | Documentar o status destes equipamentos |

## Regulamentação de EPIs Não Devolvidos

Quando um colaborador será desativado mas ainda possui EPIs:

1. Acesse a aba **EPIs** na tela de detalhes do colaborador
2. Para cada EPI não devolvido, clique em **Registrar Devolução**
3. Escolha o motivo adequado:
   - **Devolução Normal**: Se o EPI foi fisicamente devolvido
   - **Registro de Perda**: Se o EPI não foi devolvido e não será recuperado
   - **Registro de Quebra**: Se o EPI foi devolvido danificado

> **Importante:** A devolução ou baixa de todos os EPIs não é obrigatória para desativar um colaborador, mas é uma prática recomendada para manter o controle do inventário.

## Reativando um Colaborador

Para reativar um colaborador previamente desativado:

1. Na lista de colaboradores, marque a opção **Mostrar Inativos**
2. Localize o colaborador desativado (indicado com status "Inativo")
3. Clique no ícone de **Reativar** (símbolo de reciclagem)
4. Confirme a reativação no diálogo exibido

![Reativar Colaborador](../../../assets/images/reativar-colaborador.png)

## Impacto nos Relatórios e Estatísticas

A desativação de colaboradores pode afetar:

- Contagens de colaboradores ativos em dashboards
- Taxas de conformidade no uso de EPIs
- Relatórios de gastos por colaborador
- Estatísticas de rotatividade e gestão de EPIs

Ao gerar relatórios, é possível incluir ou excluir colaboradores inativos através de filtros específicos.

## Implicações Legais

Do ponto de vista legal, a desativação preserva todos os registros necessários para:

- Comprovação de entrega de EPIs durante o período de atividade
- Demonstração de conformidade com a NR-6 em fiscalizações
- Rastreabilidade em caso de investigações de acidentes
- Confirmação de treinamentos e orientações fornecidas

## Melhores Práticas

- **Planejamento Prévio**: Organize a desativação antes do desligamento oficial
- **Devolução de EPIs**: Sempre que possível, recolha todos os EPIs antes da desativação
- **Documentação**: Registre claramente o motivo da desativação
- **Data de Encerramento**: Mantenha a precisão na data de desligamento
- **Verificação Final**: Confirme que todos os registros estão corretamente documentados

## Erros Comuns e Soluções

| Erro | Solução |
|------|---------|
| "Colaborador possui solicitações em andamento" | Conclua ou cancele as solicitações pendentes |
| "Erro ao salvar data de encerramento" | Verifique se o formato da data está correto |
| "Colaborador já desativado" | Verifique se o status já foi alterado previamente |

---

*Última atualização: 16 de Maio de 2025*