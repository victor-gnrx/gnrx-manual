# Sincronização

## Sincronização

A sincronização transfere os dados do dispositivo para o servidor, criando backup seguro.

### Quando Acontece a Sincronização

#### Automática

* **Ao concluir um formulário** (se tiver internet)
* **Em algum momento posterior** quando o app detecta conexão

<figure><img src="../.gitbook/assets/image (18).png" alt=""><figcaption></figcaption></figure>

#### Manual

* **Nas configurações**: Forçar sincronização (Apenas 1x a cada 15 minutos)

<figure><img src="../.gitbook/assets/image (17).png" alt=""><figcaption></figcaption></figure>



### Como Funciona

#### Se Tem Internet na Conclusão

1. Conclui o formulário
2. App sincroniza imediatamente
3. Status muda para "ID Server: \[número]"

#### Se Não Tem Internet na Conclusão

1. Conclui o formulário
2. App marca para sincronizar depois
3. Status fica "ID Server: Não Sincronizado"
4. **Mais tarde** o app sincroniza sozinho (Volátil)

### Estados Visuais

#### "ID Server: Não Sincronizado"

* Dados apenas no seu dispositivo
* Será sincronizado automaticamente depois
* Pode forçar nas configurações

#### "ID Server: \[número]"

* Dados salvos no servidor
* Backup completo
* Seguro para outros usuários verem

#### Indicadores Coloridos

* **Verde**: Sincronizado
* **Amarelo**: Pendente
* **Vermelho**: Erro

### Como Forçar Sincronização

#### Método 1 - Configurações

1. Vá em **Configurações**
2. Procure opção de sincronização
3. Garanta que tenha internet e não tenha feito outra sincronização nos últimos 15 minutos
4. Toque para "Forçar Sincrnização"

<figure><img src="../.gitbook/assets/image (17).png" alt=""><figcaption></figcaption></figure>

### Problemas Comuns

#### Não Sincroniza

* Verificar se tem internet
* Ir nas configurações e forçar
* Aguardar - às vezes demora

#### Fica "Não Sincronizado"

* Normal quando conclui sem internet
* Será sincronizado automaticamente depois
* Pode forçar se tiver pressa

#### Erro na Sincronização

* Verificar conexão
* Tentar forçar novamente
* Se persistir, anotar erro e reportar (Buscand o erro nos logs, na configuração)
