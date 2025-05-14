---
description: Transferindo dados entre o aplicativo e o servidor
icon: refresh-cw
---

# Como Sincronizar com o Servidor

A sincronização é um processo crítico que transfere os dados coletados no aplicativo GNRX Auditorias para o servidor central, garantindo que todas as informações estejam atualizadas e disponíveis para todos os usuários do sistema. Este guia explica como realizar a sincronização corretamente e solucionar problemas comuns.

## Importância da Sincronização

A sincronização entre o aplicativo mobile e o servidor é fundamental por vários motivos:

- **Segurança dos dados**: Protege as informações contra perda em caso de problemas com o dispositivo
- **Compartilhamento**: Torna os dados acessíveis a todos os usuários autorizados no sistema web
- **Processamento**: Permite a geração de relatórios mais complexos e análises avançadas
- **Integração**: Conecta as auditorias com outros módulos do sistema (planos de ação, indicadores)
- **Backup**: Mantém cópias seguras de todas as informações coletadas

> **ALERTA CRÍTICO**: Dados que existem apenas no aplicativo (não sincronizados) serão permanentemente perdidos se o aplicativo for desinstalado, o usuário fizer logout, ou ocorrer algum problema sério com o dispositivo.

## Tipos de Dados Sincronizados

Durante a sincronização, os seguintes tipos de dados são transferidos:

**Upload (do dispositivo para o servidor)**:
- Auditorias criadas ou atualizadas
- Fotos tiradas durante as auditorias
- Assinaturas coletadas
- Respostas e observações registradas

**Download (do servidor para o dispositivo)**:
- Novos modelos de checklist
- Atualizações de configurações
- Lista atualizada de locais e usuários
- Auditorias atribuídas a você
- Atualizações de status de auditorias compartilhadas

<div style="text-align: center; margin: 20px 0;">
  <img src="https://example.com/imagens/app-fluxo-sincronizacao.png" alt="Fluxo de sincronização de dados" width="90%" />
</div>

## Quando Sincronizar

Recomendamos sincronizar o aplicativo nas seguintes situações:

1. **Antes de sair para campo**: Para garantir que tem os modelos e configurações mais recentes
2. **Imediatamente após concluir uma auditoria**: Para transferir os dados para o servidor o quanto antes
3. **Ao retornar a uma área com conexão**: Se esteve trabalhando offline
4. **Antes de sair do aplicativo ou fazer logout**: Para evitar qualquer perda de dados
5. **Periodicamente durante auditorias longas**: Para backup parcial dos dados coletados até o momento

## Verificando Auditorias Pendentes de Sincronização

Para identificar quais auditorias ainda não foram sincronizadas:

1. Na tela inicial do aplicativo, toque em "**Pendentes de Sincronização**"
2. Você verá uma lista de todas as auditorias que existem apenas no dispositivo
3. Cada item mostrará:
   - Nome da auditoria
   - Data de criação ou última modificação
   - Status (Em andamento ou Concluída)
   - Tamanho aproximado dos dados (útil para estimar o tempo de sincronização)

<div style="text-align: center; margin: 20px 0;">
  <img src="https://example.com/imagens/app-pendentes-sincronizacao.png" alt="Auditorias pendentes de sincronização" width="300" />
</div>

> **DICA**: Um contador no ícone "Pendentes de Sincronização" mostra quantas auditorias precisam ser sincronizadas. Mantenha este número baixo, sincronizando regularmente.

## Realizando a Sincronização

### Sincronização Automática

O aplicativo tenta realizar sincronização automática nas seguintes situações:

1. Ao iniciar o aplicativo (se houver conexão disponível)
2. Ao finalizar uma auditoria (se houver conexão disponível)
3. Quando o dispositivo recupera conexão com a internet após período offline
4. Nos intervalos programados nas configurações (se habilitado)

### Sincronização Manual

Para iniciar a sincronização manualmente:

1. Conecte seu dispositivo à internet (Wi-Fi ou dados móveis)
2. Acesse a tela "Pendentes de Sincronização"
3. Você tem duas opções:
   - **Sincronizar Todas**: Toque no botão "Sincronizar Todas" no topo da tela para processar todas as auditorias pendentes
   - **Sincronizar Individual**: Toque no botão "Sincronizar" ao lado de uma auditoria específica para processar apenas aquela

<div style="text-align: center; margin: 20px 0;">
  <img src="https://example.com/imagens/app-sincronizacao.png" alt="Tela de sincronização" width="300" />
</div>

4. Uma barra de progresso mostrará o status da sincronização
5. Mantenha o aplicativo aberto até a conclusão do processo
6. Após a sincronização bem-sucedida, os itens serão removidos da lista de pendentes

> **IMPORTANTE**: Durante a sincronização, especialmente de auditorias com muitas fotos, mantenha o aplicativo em primeiro plano e evite que o dispositivo entre em modo de economia de energia, pois isso pode interromper o processo.

## Monitorando o Progresso da Sincronização

Durante a sincronização de múltiplas auditorias ou auditorias extensas:

1. Uma barra de progresso geral mostra a porcentagem concluída do processo completo
2. Indicadores individuais mostram o progresso de cada auditoria
3. O aplicativo exibe informações sobre a etapa atual:
   - "Enviando dados de auditoria..."
   - "Enviando fotos (X de Y)..."
   - "Recebendo atualizações..."
4. Uma notificação persistente permite monitorar o progresso mesmo se você minimizar o aplicativo

<div style="text-align: center; margin: 20px 0;">
  <img src="https://example.com/imagens/app-progresso-sincronizacao.png" alt="Progresso da sincronização" width="300" />
</div>

## Priorização de Sincronização

Quando há múltiplas auditorias pendentes, o sistema prioriza a sincronização na seguinte ordem:

1. Auditorias concluídas (status: Finalizada)
2. Auditorias em andamento mais recentes
3. Auditorias com menos dados (fotos) para transferência mais rápida

Você pode alterar manualmente esta priorização sincronizando individualmente as auditorias mais importantes primeiro.

## Verificando o Status de Sincronização

Para confirmar se uma auditoria foi sincronizada corretamente:

1. Na lista principal de auditorias, verifique o ícone de status:
   - **Nuvem com check**: Totalmente sincronizada com o servidor
   - **Nuvem com seta para cima**: Pendente de sincronização
   - **Nuvem com alerta**: Erro na última tentativa de sincronização

2. Para ver detalhes mais específicos de uma auditoria:
   - Abra a auditoria e toque em "Detalhes"
   - Verifique o campo "Status de Sincronização"
   - Se sincronizada, verá a data e hora da última sincronização bem-sucedida

<div style="text-align: center; margin: 20px 0;">
  <img src="https://example.com/imagens/app-status-sincronizacao.png" alt="Ícones de status de sincronização" width="300" />
</div>

## Otimizando a Sincronização

Para tornar o processo de sincronização mais rápido e eficiente:

1. **Use Wi-Fi sempre que possível**: A transferência é mais rápida e não consome seu plano de dados
2. **Sincronize regularmente**: Evite acumular muitas auditorias pendentes
3. **Controle a qualidade das fotos**: Ajuste nas configurações para equilibrar qualidade e tamanho
4. **Priorize auditorias importantes**: Sincronize manualmente as mais críticas primeiro
5. **Mantenha o aplicativo atualizado**: Novas versões frequentemente incluem melhorias no processo de sincronização
6. **Libere espaço no dispositivo**: Mais espaço disponível ajuda no processamento de dados

## Configurações de Sincronização

Para personalizar o comportamento da sincronização:

1. Acesse "**Configurações**" no menu principal
2. Selecione "**Configurações de Sincronização**"
3. Ajuste as seguintes opções conforme necessário:
   - **Sincronização automática**: Ativar/desativar
   - **Apenas em Wi-Fi**: Restringir sincronização automática apenas a redes Wi-Fi
   - **Intervalo de sincronização**: Frequência das verificações automáticas
   - **Compressão de fotos**: Nível de compressão para transferência mais rápida
   - **Notificações**: Alertas sobre status de sincronização
   - **Prioridade de sincronização**: Critérios para ordenar a fila

<div style="text-align: center; margin: 20px 0;">
  <img src="https://example.com/imagens/app-configuracoes-sincronizacao.png" alt="Configurações de sincronização" width="300" />
</div>

## Sincronização Parcial

Em situações com conexão limitada ou instável, você pode optar pela sincronização parcial:

1. Toque e segure sobre uma auditoria na lista de pendentes
2. Selecione "**Opções Avançadas**"
3. Escolha "**Sincronização Parcial**"
4. Selecione quais componentes deseja sincronizar:
   - Dados básicos da auditoria (respostas, observações)
   - Fotos (selecione todas ou apenas específicas)
   - Assinaturas

> **NOTA**: Uma auditoria parcialmente sincronizada ainda aparecerá na lista de pendentes até que todos os seus componentes sejam transferidos.

## Resolução de Problemas de Sincronização

### Erro de Conexão

Se ocorrer um erro devido a problemas de conexão:

1. Verifique sua conexão com a internet
2. Teste abrir um site em seu navegador para confirmar o acesso
3. Mude para uma rede diferente, se possível (Wi-Fi para dados móveis ou vice-versa)
4. Tente sincronizar novamente após confirmar a conexão

### Sincronização Interrompida

Se o processo for interrompido no meio:

1. O sistema marcará automaticamente a auditoria para ser retomada
2. Na próxima tentativa, a sincronização continuará de onde parou
3. Não é necessário reenviar dados já transferidos

### Conflitos de Dados

Em raras situações, podem ocorrer conflitos quando a mesma auditoria é editada em diferentes dispositivos:

1. O sistema detectará o conflito durante a sincronização
2. Você receberá uma notificação com as opções:
   - **Manter versão do servidor**: Descarta as alterações locais
   - **Usar versão do dispositivo**: Substitui os dados do servidor
   - **Revisão manual**: Permite comparar as diferenças e decidir por item

### Erro "Armazenamento Insuficiente no Servidor"

Se o servidor atingir limites de armazenamento:

1. Entre em contato com o administrador do sistema
2. Temporariamente, tente sincronizar com qualidade reduzida de fotos
3. Sincronize apenas os dados básicos, sem fotos, até que o problema seja resolvido

## Relatório de Sincronização

Após cada processo completo de sincronização, um relatório estará disponível:

1. Toque em "**Histórico de Sincronização**" no menu de configurações
2. Selecione a data desejada para ver detalhes
3. O relatório mostrará:
   - Auditorias sincronizadas com sucesso
   - Itens que falharam (se houver)
   - Tempo total do processo
   - Volume de dados transferidos
   - Erros específicos encontrados (se houver)

Este relatório é útil para diagnóstico em caso de problemas recorrentes.

## Comportamento Após a Sincronização

Após uma sincronização bem-sucedida:

1. As auditorias sincronizadas ainda ficam disponíveis no dispositivo para consulta
2. Auditorias finalizadas ficam bloqueadas para edição
3. Auditorias em andamento podem continuar sendo editadas
4. As mesmas auditorias agora estão acessíveis no sistema web
5. Notificações relevantes são enviadas aos envolvidos (se configurado)

> **DICA**: Mesmo após a sincronização, mantenha as auditorias importantes no dispositivo para consulta rápida em campo. O aplicativo permite você mantenha o acesso offline as auditorias que precisam ser editadas.