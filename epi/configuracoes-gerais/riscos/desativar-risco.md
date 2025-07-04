---
icon: burst
---

# Desativar Risco

## Introdução

A funcionalidade de desativação permite remover riscos ocupacionais personalizados da utilização ativa no sistema, sem perder o histórico de registros relacionados a eles. Esta operação é útil quando um risco específico deixa de ser relevante para as operações da empresa ou foi cadastrado incorretamente.

<figure><img src="../../.gitbook/assets/image (60).png" alt=""><figcaption></figcaption></figure>

## Limitações Importantes

**Atenção**: Assim como na edição, apenas riscos personalizados (criados pela própria empresa) podem ser desativados. Os riscos pré-configurados do sistema base não permitem desativação, pois são essenciais para a conformidade do GNRX com as normas regulamentadoras.

## Como Acessar

Para desativar um risco ocupacional personalizado:

1. Acesse o menu **Configurações** na barra de navegação principal
2. Selecione a opção **Riscos** no submenu que se abre
3. Localize o risco personalizado que deseja desativar na lista
4. Clique no ícone de desativação (Block) na coluna "Opções" do risco desejado

Se o ícone de desativação não estiver disponível, isto indica que o risco faz parte da base pré-configurada e não pode ser desativado.

## Modal de Confirmação

Ao clicar no ícone de desativação, um modal de confirmação será exibido:

* **Mensagem**: "Tem certeza que deseja inativar este risco?"
* **Botão "Cancelar"**: Fecha o modal sem realizar qualquer alteração
* **Botão "Inativar"**: Confirma a desativação do risco selecionado

Este modal é uma medida de segurança para evitar desativações acidentais.

## Passo a Passo para Desativar um Risco

### 1. Verificar Associações

Antes de desativar um risco, é recomendável verificar:

* Se o risco está associado a algum GHE ativo
* Se existem EPIs vinculados especificamente a este risco
* Se há documentações recentes que referenciam este risco

### 2. Iniciar o Processo de Desativação

1. Localize o risco na lista de riscos ocupacionais
2. Clique no ícone de desativação (block) na coluna "Opções"

### 3. Confirmar a Desativação

1. No modal de confirmação, verifique se está desativando o risco correto
2. Clique no botão **Inativar** para confirmar a operação
3. Aguarde a mensagem de confirmação do sistema

## Impacto da Desativação

Ao desativar um risco ocupacional, ocorrem as seguintes consequências:

* **Visibilidade**: O risco deixa de aparecer na lista padrão de riscos ativos
* **Seleção**: O risco não pode mais ser selecionado para novos GHEs ou documentações
* **Associações existentes**: GHEs que já utilizavam o risco manterão a associação histórica
* **Relatórios**: O risco continuará aparecendo em relatórios históricos anteriores à desativação

## Diferença entre Desativar e Excluir

É importante entender que desativar um risco não é o mesmo que excluí-lo permanentemente:

* **Desativação**: O risco é marcado como inativo, mas permanece no banco de dados
* **Exclusão**: Remoção completa do registro (não disponível no GNRX para preservar o histórico)

A desativação é preferível à exclusão pois preserva a integridade dos registros históricos e a rastreabilidade das informações.

## Reativação de Riscos

Caso seja necessário reativar um risco previamente desativado:

1. Entre em contato com o suporte técnico do GNRX
2. Informe o nome e ID do risco a ser reativado
3. Justifique a necessidade de reativação

A funcionalidade de reativação não está disponível diretamente na interface do usuário para evitar oscilações frequentes no status dos riscos.

## Boas Práticas

Para gerenciar a desativação de riscos de forma eficaz:

* **Documentação**: Registre internamente os motivos da desativação
* **Comunicação**: Informe a equipe de saúde e segurança sobre riscos desativados
* **Avaliação prévia**: Analise cuidadosamente o impacto da desativação antes de executá-la
* **Uso criterioso**: Desative apenas riscos que realmente não são mais aplicáveis

## Considerações Finais

* A desativação de riscos deve ser uma operação realizada com cautela e planejamento
* Prefira editar um risco em vez de desativá-lo quando apenas ajustes forem necessários
* Mantenha um registro interno das decisões de desativação para referência futura

***

_Última atualização: 18 de Maio de 2025_
