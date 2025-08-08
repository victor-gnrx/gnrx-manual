# Estados e Status

O aplicativo utiliza indicadores visuais claros para comunicar o estado dos formulários e registros, facilitando o entendimento do status de sincronização e disponibilidade.

## Estados de Formulários

### Ativo

* **Cor**: Verde
* **Significado**: Formulário disponível para uso
* **Funcionalidades**: Aceita novos registros, permite edição
* **Sincronização**: Inativa

### Concluído

* **Cor**: GNRx
* **Significado**: Formulário pronto para sincronização/sincronizado
* **Funcionalidades**: Apenas visualização, sem novos registros e edição
* **Sincronização**: Realizada / Próxima de realizar

## Status de Sincronização

### Sincronizado

* **Descrição**: "ID Server: \[número]"
* **Significado**: Dados salvos com sucesso no servidor
* **Backup**: Completo e seguro

### Não Sincronizado

* **Descrição**: "ID Server: Não Sincronizado"
* **Significado**: Dados apenas no dispositivo local
* **Ação necessária**: Sincronizar quando possível

