# Estados e Status

O aplicativo utiliza indicadores visuais claros para comunicar o estado dos formulários e registros, facilitando o entendimento do status de sincronização e disponibilidade.

## Estados de Formulários

### Ativo
- **Cor**: Verde
- **Significado**: Formulário disponível para uso
- **Funcionalidades**: Aceita novos registros, permite edição
- **Sincronização**: Ativa e automática

### Inativo
- **Cor**: Vermelho
- **Significado**: Formulário temporariamente desabilitado
- **Funcionalidades**: Apenas visualização, sem novos registros
- **Sincronização**: Mantida para dados existentes

### Padrão
- **Cor**: Amarelo
- **Significado**: Formulário modelo da empresa
- **Funcionalidades**: Base para criação de outros formulários
- **Uso**: Template e referência

## Estados de Sincronização

### Sincronizado
- **Indicador**: Verde
- **Descrição**: "ID Server: [número]"
- **Significado**: Dados salvos com sucesso no servidor
- **Backup**: Completo e seguro

### Não Sincronizado
- **Indicador**: Vermelho
- **Descrição**: "ID Server: Não Sincronizado"
- **Significado**: Dados apenas no dispositivo local
- **Ação necessária**: Sincronizar quando possível

### Pendente
- **Indicador**: Amarelo
- **Descrição**: Status de aguardo
- **Significado**: Na fila para sincronização
- **Ação automática**: Enviará quando houver conexão

### Falha
- **Indicador**: Vermelho com ícone de erro
- **Descrição**: Erro durante sincronização
- **Significado**: Problema na transmissão dos dados
- **Ação necessária**: Verificar e tentar novamente

## Estados de Registros

### Rascunho
- **Indicador**: Cinza ou específico do app
- **Significado**: Preenchimento em andamento
- **Dados**: Salvos localmente
- **Edição**: Permitida

### Concluído
- **Indicador**: Conforme sincronização
- **Significado**: Preenchimento finalizado
- **Próxima etapa**: Aguardando ou realizada sincronização

### Validado
- **Indicador**: Verde
- **Significado**: Dados verificados e aprovados
- **Status**: Final no processo

## Indicadores Visuais

### Cores do Sistema
- **Verde**: Situação normal, sucesso
- **Amarelo**: Atenção, aguardando ação
- **Vermelho**: Erro, ação necessária
- **Cinza**: Inativo, neutro

### Ícones Complementares
- **Nuvem com check**: Sincronizado
- **Nuvem com seta**: Sincronizando
- **Nuvem com X**: Erro de sincronização
- **Dispositivo**: Apenas local

## Transições de Estado

### Fluxo Normal de Formulário
1. **Criação**: Estado inicial (Ativo)
2. **Uso operacional**: Mantém estado Ativo
3. **Finalização**: Pode ir para Inativo
4. **Arquivamento**: Estado final

### Fluxo Normal de Registro
1. **Iniciado**: Estado Rascunho
2. **Preenchimento**: Mantém Rascunho
3. **Finalização**: Estado Concluído
4. **Sincronização**: Estado Sincronizado

### Fluxo de Sincronização
1. **Local**: Dados apenas no dispositivo
2. **Pendente**: Na fila de sincronização
3. **Enviando**: Transmissão em andamento
4. **Sincronizado**: Confirmado no servidor

## Monitoramento de Status

### Verificação Visual
- **Lista de formulários**: Status em cada item
- **Detalhes do formulário**: Status consolidado
- **Lista de registros**: Status individual

### Atualização de Status
- **Automática**: Durante sincronização
- **Manual**: Puxar tela para baixo
- **Em tempo real**: Mudanças imediatas

### Notificações
- **Sincronização concluída**: Confirmação visual
- **Erros**: Alertas específicos
- **Status críticos**: Avisos importantes

## Interpretação de Status

### Status Normais
- **Verde em tudo**: Sistema funcionando normalmente
- **Alguns amarelos**: Sincronização pendente normal
- **Mistura controlada**: Operação típica

### Status de Atenção
- **Muitos pendentes**: Verificar conexão
- **Alguns vermelhos**: Erros pontuais a corrigir
- **Padrão diferente**: Investigar causa

### Status Críticos
- **Tudo vermelho**: Problema de conectividade
- **Nada sincroniza**: Verificar configurações
- **Perda de dados**: Ação imediata necessária

## Resolução por Status

### Para Status Pendente
1. **Verificar conexão** com internet
2. **Aguardar sincronização** automática
3. **Forçar sincronização** se necessário

### Para Status de Erro
1. **Verificar conexão** de rede
2. **Verificar dados** inseridos
3. **Tentar novamente** após correção
4. **Contatar suporte** se persistir

### Para Status Não Sincronizado
1. **Conectar à internet** se offline
2. **Iniciar sincronização** manual
3. **Verificar permissões** de rede
4. **Aguardar processamento** completo