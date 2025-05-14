---
description: Preenchendo itens no checklist de auditoria
icon: check-square
---

# Como Preencher uma Auditoria

Este guia explica como realizar o preenchimento de itens em uma auditoria no aplicativo GNRX Auditorias, desde a navegação pelas seções até a avaliação de conformidade dos itens.

## Visão Geral da Tela de Preenchimento

Após iniciar uma auditoria, você verá a tela de preenchimento do checklist com os seguintes elementos:

<div style="text-align: center; margin: 20px 0;">
  <img src="https://example.com/imagens/app-preenchimento.png" alt="Tela de preenchimento de auditoria" width="300" />
</div>

1. **Barra Superior**: Exibe o nome da auditoria e botões de ação
2. **Seletor de Seções**: Permite navegar entre as diferentes seções do checklist
3. **Barra de Progresso**: Mostra o percentual de itens já respondidos
4. **Lista de Itens**: Exibe os itens da seção atual a serem avaliados
5. **Botões de Navegação**: Permitem avançar ou retornar entre as seções
6. **Botão de Salvar**: Armazena o progresso atual da auditoria

## Navegação pelas Seções

Os checklists são organizados em seções para facilitar o preenchimento:

### Usando o Seletor de Seções

1. Toque no nome da seção atual no topo da tela
2. Aparecerá um menu suspenso com todas as seções disponíveis
3. Selecione a seção que deseja acessar
4. A tela será atualizada para mostrar os itens da seção selecionada

### Usando Gestos de Deslize

1. Deslize a tela horizontalmente para navegar entre seções
2. Deslize para a esquerda para ir à próxima seção
3. Deslize para a direita para retornar à seção anterior

### Usando os Botões de Navegação

1. Toque no botão "Próxima" na parte inferior da tela para avançar
2. Toque no botão "Anterior" para retornar à seção precedente

> **DICA**: Uma pequena representação visual no topo da tela indica a sua posição atual no fluxo de seções e o progresso geral.

## Avaliando os Itens do Checklist

Para cada item do checklist, você precisa indicar o estado de conformidade:

### Opções de Conformidade

1. Toque em uma das opções disponíveis para o item:
   - **Conforme** (Verde): O item atende completamente aos requisitos
   - **Não Conforme** (Vermelho): O item não atende aos requisitos
   - **Não Aplicável** (Cinza): O item não se aplica à situação atual
   - **Não Avaliado** (Branco): O item não foi verificado nesta auditoria

<div style="text-align: center; margin: 20px 0;">
  <img src="https://example.com/imagens/app-opcoes-conformidade.png" alt="Opções de conformidade" width="300" />
</div>

### Respondendo Itens "Não Conforme"

Quando um item é marcado como "Não Conforme", campos adicionais são exibidos:

1. **Nível de Criticidade**: Selecione a gravidade da não conformidade
   - Baixa: Representa um problema menor, com impacto limitado
   - Média: Representa um problema significativo que requer atenção
   - Alta: Representa um problema grave que exige ação imediata

2. **Detalhes da Não Conformidade**: Descreva o problema encontrado
   - Seja claro e específico sobre a situação
   - Mencione o local exato e as condições observadas

3. **Ação Corretiva Recomendada**: Sugira como resolver o problema
   - Este campo pode vir pré-preenchido conforme configuração do modelo
   - Você pode editar ou complementar a sugestão

4. **Prazo para Correção**: Defina até quando a correção deve ser realizada
   - Toque no campo para abrir o seletor de data
   - Considere a criticidade ao definir o prazo

5. **Responsável pela Correção** (se disponível):
   - Selecione quem ficará encarregado de implementar a ação corretiva
   - A lista exibe os usuários cadastrados no sistema

<div style="text-align: center; margin: 20px 0;">
  <img src="https://example.com/imagens/app-nao-conforme.png" alt="Detalhamento de não conformidade" width="300" />
</div>

## Lidando com Subitens e Itens Hierárquicos

Alguns checklists possuem estrutura hierárquica, com itens principais e subitens:

1. Itens com subitens exibem um indicador de expansão (seta ou ícone +)
2. Toque no item principal para expandir ou recolher seus subitens
3. Em alguns modelos, a conformidade do item principal depende automaticamente dos subitens:
   - Se todos os subitens forem "Conforme", o item principal será marcado como "Conforme"
   - Se qualquer subitem for "Não Conforme", o item principal também será "Não Conforme"
   - Em outros modelos, cada item é avaliado independentemente

<div style="text-align: center; margin: 20px 0;">
  <img src="https://example.com/imagens/app-subitens.png" alt="Itens hierárquicos e subitens" width="300" />
</div>

## Filtrando e Buscando Itens

Para auditorias com muitos itens, você pode usar recursos de filtro e busca:

1. Toque no ícone de filtro (funil) na barra superior
2. Selecione as opções de filtro desejadas:
   - Status de resposta (respondidos/não respondidos)
   - Conformidade (conforme/não conforme/não aplicável)
   - Criticidade (para itens não conformes)

Para buscar itens específicos:
1. Toque no ícone de lupa na barra superior
2. Digite o texto que deseja encontrar
3. Os itens que contêm o texto pesquisado serão destacados
4. Use as setas para navegar entre os resultados encontrados

## Itens Obrigatórios e Condicionais

Os checklists podem incluir itens com regras específicas:

1. **Itens Obrigatórios**: Marcados com asterisco (*) e precisam ser respondidos para finalizar a auditoria
2. **Itens Condicionais**: Aparecem ou desaparecem dependendo das respostas a outros itens
   - Por exemplo, ao marcar um item sobre "Trabalho em Altura" como aplicável, podem surgir itens adicionais específicos sobre este tema

## Salvando o Progresso

É importante salvar seu trabalho regularmente durante o preenchimento:

1. Toque no botão "Salvar" (geralmente localizado na parte inferior da tela)
2. Uma mensagem confirmará o salvamento bem-sucedido
3. A auditoria permanecerá com status "Em andamento"
4. Você pode continuar o preenchimento ou sair e retornar posteriormente

> **IMPORTANTE**: No modo offline, os dados são salvos apenas no dispositivo. Sincronize assim que possível para transferir as informações para o servidor.

### Salvamento Automático

O aplicativo realiza salvamento automático nas seguintes situações:
- A cada 5 minutos durante o uso ativo
- Ao mudar para outra seção do checklist
- Quando o aplicativo vai para segundo plano
- Antes de iniciar a sincronização

## Acompanhando o Progresso

Durante o preenchimento, você pode acompanhar seu progresso:

1. A barra de progresso no topo da tela mostra o percentual de itens respondidos
2. No menu de seções, um indicador visual mostra quais seções já foram totalmente preenchidas
3. Seções com itens obrigatórios não respondidos são marcadas com um símbolo de atenção

<div style="text-align: center; margin: 20px 0;">
  <img src="https://example.com/imagens/app-progresso.png" alt="Indicadores de progresso" width="300" />
</div>

## Continuando uma Auditoria em Andamento

Para retomar o preenchimento de uma auditoria salva:

1. Na tela inicial, acesse "Minhas Auditorias"
2. Localize a auditoria com status "Em andamento"
3. Toque na auditoria para abri-la
4. O aplicativo carregará a última seção que você estava preenchendo
5. Continue o preenchimento de onde parou

## Dicas para um Preenchimento Eficiente

- **Prepare-se antes**: Familiarize-se com o modelo de checklist antes de iniciar a auditoria
- **Siga uma sequência lógica**: Complete uma seção por vez, na ordem apresentada
- **Documente adequadamente**: Adicione fotos e observações detalhadas, especialmente para não conformidades
- **Salve regularmente**: Evite perda de trabalho salvando seu progresso frequentemente
- **Use dois dispositivos, se possível**: Um para consultar o checklist e outro para tirar fotos
- **Priorize itens críticos**: Em auditorias extensas, comece pelos itens de maior impacto
- **Trabalhe offline conscientemente**: Lembre-se de sincronizar assim que houver conexão disponível

## Solução de Problemas Comuns

### Itens não estão sendo salvos
- Verifique se há ícones de erro ao lado dos itens
- Certifique-se de preencher todos os campos obrigatórios para itens não conformes
- Tente salvar manualmente antes de mudar de seção

### Não consigo avançar para a próxima seção
- Verifique se há itens obrigatórios não respondidos na seção atual
- Reinicie o aplicativo se os botões de navegação não estiverem respondendo
- Verifique se o aplicativo está atualizado para a versão mais recente

### Tela congelando durante o preenchimento
- Dispositivos com pouca memória podem apresentar lentidão
- Feche outros aplicativos em execução
- Reinicie o aplicativo ou o dispositivo

## Próximos Passos

Após preencher os itens do checklist, você pode complementar com evidências fotográficas e observações:

- [Como Tirar Fotos e Anexar Evidências](/auditorias/aplicativo/tirar-fotos.md)
- [Como Adicionar Observações](/auditorias/aplicativo/adicionar-observacoes.md)
- [Finalizando e Enviando a Auditoria](/auditorias/aplicativo/finalizar-enviar.md)