---
description: Transferindo dados entre o aplicativo e o servidor
icon: arrows-rotate
---

# Como Sincronizar com o Servidor

A sincronização é um processo crítico que transfere os dados coletados no aplicativo GNRx - Auditorias para o servidor central, garantindo que todas as informações estejam atualizadas e disponíveis para todos os usuários do sistema. Este guia explica como realizar a sincronização corretamente e solucionar problemas comuns.

## Importância da Sincronização da Auditoria

A sincronização entre o aplicativo mobile e o servidor é fundamental por vários motivos:

* **Segurança dos dados**: Protege as informações contra perda em caso de problemas com o dispositivo
* **Compartilhamento**: Torna os dados acessíveis a todos os usuários autorizados no sistema web
* **Processamento**: Permite a geração de relatórios mais complexos e análises avançadas
* **Backup**: Mantém cópias seguras de todas as informações coletadas

> **ALERTA CRÍTICO**: Dados que existem apenas no aplicativo (não sincronizados) serão permanentemente perdidos se o aplicativo for desinstalado, o usuário fizer logout, ou ocorrer algum problema sério com o dispositivo.

## Tipos de Dados Sincronizados

Durante a sincronização, os seguintes tipos de dados são transferidos:

**Upload (do dispositivo para o servidor)**:

* Auditorias criadas ou atualizadas
* Fotos tiradas durante as auditorias
* Localizações
* Assinaturas coletadas
* Respostas e observações registradas

![Fluxo de sincronização de dados](https://example.com/imagens/app-fluxo-sincronizacao.png)

## Quando Sincronizar

Recomendamos sincronizar o aplicativo nas seguintes situações:

1. **Imediatamente após concluir uma auditoria**: Para transferir os dados para o servidor o quanto antes
2. **Ao retornar a uma área com conexão**: Se esteve trabalhando offline
3. **Periodicamente durante auditorias longas**: Para backup parcial dos dados coletados até o momento

## Verificando Auditorias Pendentes de Sincronização

Para identificar quais auditorias ainda não foram sincronizadas:

Na tela inicial do aplicativo, Minhas Auditorias, as auditorias que não foram sincronizadas estarão com status **"N/S"** (Não Sincronizada)

![Auditorias pendentes de sincronização](https://example.com/imagens/app-pendentes-sincronizacao.png)

## Realizando a Sincronização

Para iniciar a sincronização de uma auditoria:

1. Conecte seu dispositivo à internet (Wi-Fi ou dados móveis)
2. Acesse a tela da auditoria que deseja sincronizar
3. Aqui você tem 2 opções:
   * **Clicar no botão "Gerar Relatório"**: Que abrirá a tela de relatório / sincronização
   * **Clicar em Inciar Auditoria => Menu => Relatório**: Que também abrirá a tela de relatório / sincronização
4. Verifique se o progresso está correto
5. Caso queira enviar email / solicitar assinaturas remotas, deixe a opção "Enviar relatório por e-mail" marcada
   * Os emails serão enviados para os destinatários configurados pelo sistema web. Pelo usuário administrador.
   * Também é enviado para o email do usuário que iniciou a auditoria.
6. Na tela de relatório / sincronização, clique em "Atualizar Servidor"

![Tela de sincronização](https://example.com/imagens/app-sincronizacao.png)

7. Uma barra de progresso mostrará o status da sincronização
8. Mantenha o aplicativo aberto até a conclusão do processo
9. Após a sincronização bem-sucedida, será exibida uma mensagem de confirmação

> **IMPORTANTE**: Durante a sincronização, especialmente de auditorias com muitas fotos, mantenha o aplicativo em primeiro plano e evite que o dispositivo entre em modo de economia de energia, pois isso pode interromper o processo.

## Monitorando o Progresso da Sincronização

Durante a sincronização de múltiplas auditorias ou auditorias extensas:

1. Uma barra de progresso geral mostra a porcentagem concluída do processo completo
2. Indicadores individuais mostram o progresso de cada auditoria
3. O aplicativo exibe informações sobre a etapa atual:
   * "Enviando dados de auditoria..."
   * "Enviando fotos (X de Y)..."

![Progresso da sincronização](https://example.com/imagens/app-progresso-sincronizacao.png)

## Otimizando a Sincronização

Para tornar o processo de sincronização mais rápido e eficiente:

1. **Use Wi-Fi sempre que possível**: A transferência é mais rápida e não consome seu plano de dados
2. **Sincronize regularmente**: Evite acumular muitas fotos pendentes
3. **Priorize auditorias importantes**: Sincronize manualmente as mais críticas primeiro
4. **Mantenha o aplicativo atualizado**: Novas versões frequentemente incluem melhorias no processo de sincronização
5. **Libere espaço no dispositivo**: Mais espaço disponível ajuda no processamento de dados

## Resolução de Problemas de Sincronização

### Erro de Conexão

Se ocorrer um erro devido a problemas de conexão:

1. Verifique sua conexão com a internet
2. Teste abrir um site em seu navegador para confirmar o acesso
3. Mude para uma rede diferente, se possível (Wi-Fi para dados móveis ou vice-versa)
4. Tente sincronizar novamente após confirmar a conexão

### Sincronização Interrompida

Se o processo for interrompido no meio:

1. Na próxima tentativa, a sincronização continuará de onde parou
2. Não é necessário reenviar dados já transferidos

### Conflitos de Dados

Em caso de alterações de dados no sistema web, o aplicativo não reconhecerá a alteração.

## Comportamento Após a Sincronização

Após uma sincronização bem-sucedida:

1. As auditorias sincronizadas ainda ficam disponíveis no dispositivo para consulta
2. Auditorias em andamento podem continuar sendo editadas
3. As mesmas auditorias agora estão acessíveis no sistema web
4. Emails enviados para os destinatários configurados pelo sistema web
5. Assinaturas remotas são enviadas para os destinatários configurados pelo sistema web
6. Relatório da auditoria estará disponível no sistema web

> **DICA**: Mesmo após a sincronização, mantenha as auditorias importantes no dispositivo para consulta rápida em campo. O aplicativo permite você mantenha o acesso offline as auditorias que precisam ser editadas.
