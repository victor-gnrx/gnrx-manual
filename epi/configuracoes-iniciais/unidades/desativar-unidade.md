# Desativar Unidade

Esta página explica como desativar uma unidade existente no Sistema GNRX Gestão de EPI, bem como as implicações desta ação.

## Visão Geral

A desativação de unidades é utilizada quando uma localidade física não está mais operacional, mas você deseja manter seu histórico no sistema. Ao contrário da exclusão definitiva, a desativação preserva todos os registros associados para fins de auditoria e consulta.

## Quando Desativar uma Unidade

As situações mais comuns para desativação incluem:

- Fechamento definitivo da localidade
- Fusão de duas ou mais unidades
- Reorganização estrutural da empresa
- Suspensão temporária das operações
- Substituição por nova unidade

## Acessando a Função de Desativação

Existem duas formas de acessar a desativação de uma unidade:

### Opção 1: A partir da Lista de Unidades

1. No menu lateral, clique em **Estruturas**
2. Selecione **Unidades**
3. Na lista de unidades, localize a unidade desejada
4. Clique no ícone de **Excluir/Desativar** (símbolo de lixeira) na coluna de ações

![Desativar via Lista](../../../assets/images/desativar-unidade-lista.png)

### Opção 2: A partir da Tela de Detalhes

1. Acesse a tela de detalhes da unidade
2. Clique no botão de menu (três pontos verticais) no canto superior direito
3. Selecione a opção **Desativar Unidade**

![Desativar via Detalhes](../../../assets/images/desativar-unidade-detalhes.png)

## Processo de Desativação

Ao iniciar a desativação, o sistema apresentará um diálogo de confirmação:

![Diálogo de Confirmação](../../../assets/images/dialogo-confirmacao-desativacao.png)

O diálogo inclui:

1. Alerta sobre as consequências da desativação
2. Informações sobre itens associados (colaboradores, setores, GHEs)
3. Campo para informar o motivo da desativação (opcional, mas recomendado)
4. Botões de "Cancelar" e "Confirmar Desativação"

Para prosseguir:
1. Preencha o motivo da desativação (recomendado para fins de auditoria)
2. Clique em **Confirmar Desativação**
3. O sistema processará a solicitação e exibirá uma mensagem de confirmação

## Impacto da Desativação

Quando uma unidade é desativada:

### O que acontece:
- A unidade recebe o status "Inativo" na lista de unidades
- Ela deixa de aparecer em listas de seleção para novas associações
- Relatórios padrão filtram a unidade, a menos que explicitamente incluída
- O histórico completo permanece acessível para consulta

### O que NÃO acontece:
- O registro da unidade não é excluído do banco de dados
- Históricos de entregas de EPIs não são removidos
- Vínculos existentes com colaboradores e setores são mantidos, mas marcados como inativos
- Documentos e registros legais permanecem intactos

## Verificações Prévias à Desativação

Antes de desativar uma unidade, o sistema verifica:

| Item | Verificação | Ação Recomendada |
|------|-------------|------------------|
| **Colaboradores Ativos** | Se há funcionários ativos vinculados à unidade | Transferir para outras unidades ou desativar |
| **Solicitações Pendentes** | Se existem solicitações de EPIs em aberto | Concluir ou cancelar solicitações |
| **Estoque Disponível** | Se há EPIs em estoque nesta unidade | Transferir para outras unidades |
| **GHEs Exclusivos** | Se existem GHEs exclusivos desta unidade | Revisar e realocar se necessário |

## Reativando uma Unidade

Para reativar uma unidade previamente desativada:

1. Na lista de unidades, marque a opção **Mostrar Inativos**
2. Localize a unidade desativada (indicada com status "Inativo")
3. Clique no ícone de **Reativar** (símbolo de reciclagem)
4. Confirme a reativação no diálogo exibido

![Reativar Unidade](../../../assets/images/reativar-unidade.png)

## Considerações Importantes

- A desativação é diferente da exclusão definitiva, que não é permitida para unidades com histórico
- Relatórios históricos continuam mostrando a unidade para períodos em que estava ativa
- Para fins de conformidade legal, o histórico de EPIs de unidades desativadas permanece acessível
- Coordene com o departamento de TI antes de desativar unidades com grande volume de registros

## Alternativas à Desativação

Em alguns casos, existem alternativas preferíveis à desativação:

- **Renomeação**: Se apenas o nome mudou, edite a unidade em vez de desativá-la
- **Relocalização**: Se a unidade mudou de endereço, atualize os dados cadastrais
- **Reorganização**: Se houve fusão, considere manter uma das unidades e transferir os registros

## Logs e Auditoria

O sistema mantém registros detalhados das desativações:

- Data e hora da desativação
- Usuário que executou a ação
- Motivo informado
- Estado dos vínculos no momento da desativação

Estes logs estão disponíveis para administradores do sistema na seção de Auditoria.

---

*Última atualização: 16 de Maio de 2025*