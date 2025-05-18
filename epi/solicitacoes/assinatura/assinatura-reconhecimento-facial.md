# Assinatura com Reconhecimento Facial

Esta página explica o processo de assinatura com reconhecimento facial para confirmação de recebimento de EPIs no Sistema GNRX.

## Visão Geral

A assinatura com reconhecimento facial representa o método mais avançado e seguro para documentar o recebimento de EPIs, proporcionando alto nível de segurança jurídica tanto para a empresa quanto para o colaborador.

Esta modalidade combina a assinatura digital com a verificação biométrica facial do colaborador, garantindo que apenas a pessoa autorizada possa confirmar o recebimento dos equipamentos.

## Pré-requisitos

- Colaborador com cadastro de reconhecimento facial previamente realizado
- Solicitação com status "Em Entrega"
- Dispositivo com câmera frontal (computador, tablet ou smartphone)
- Ambiente com iluminação adequada

> **Nota:** Se o colaborador ainda não possuir cadastro facial, consulte [Cadastrar Face](../../configuracoes-iniciais/reconhecimento-facial/cadastrar-face.md) para realizar o registro antes de prosseguir.

## Processo de Assinatura com Reconhecimento Facial

### Etapa 1: Iniciar Assinatura

![Iniciar Assinatura Facial](../../../assets/images/iniciar-assinatura-facial.png)

1. Após confirmar os itens na [entrega](../entrega/confirmar-entrega.md), clique em **Prosseguir para Assinatura**
2. O sistema exibirá o Termo de Responsabilidade com a lista detalhada dos EPIs entregues
3. Selecione a opção **Assinatura com Reconhecimento Facial**
4. Clique em **Iniciar Verificação**

### Etapa 2: Verificação Facial

![Verificação Facial](../../../assets/images/verificacao-facial.png)

1. O sistema solicitará permissão para acessar a câmera (conceda a permissão)
2. Posicione o colaborador em frente à câmera, seguindo as orientações na tela:
   - Face centralizada no enquadramento
   - Boa iluminação, preferencialmente natural
   - Expressão neutra, olhando diretamente para a câmera
3. O sistema capturará automaticamente a imagem quando o posicionamento estiver adequado
4. Em seguida, processará a verificação comparando com o cadastro facial do colaborador

### Etapa 3: Confirmação e Finalização

![Confirmação de Assinatura](../../../assets/images/confirmacao-assinatura-facial.png)

1. Após reconhecimento bem-sucedido, o sistema exibirá uma mensagem de confirmação
2. O colaborador deve revisar o termo de responsabilidade na tela
3. Para concluir, o colaborador clica em **Confirmar Recebimento**
4. O sistema registrará a assinatura biométrica e finalizará o processo

## Segurança e Validação Legal

A assinatura com reconhecimento facial possui excepcional valor legal devido a:

- **Autenticação Biométrica**: Identificação positiva do colaborador através de características faciais únicas
- **Não-repúdio**: Impossibilidade técnica de negar a autoria da assinatura
- **Evidência Digital Robusta**: Combinação de múltiplos fatores de autenticação
- **Registro Imutável**: Armazenamento criptografado e à prova de adulteração
- **Trilha de Auditoria**: Registro detalhado de data, hora, localização e dispositivo

## Visualizando Registros de Assinatura Facial

Os registros de assinatura com reconhecimento facial são identificados com um ícone especial em:

1. **Ficha de EPI Digital**: na seção de histórico do colaborador
2. **Detalhes da Solicitação**: ao visualizar a solicitação específica
3. **Relatórios de Conformidade**: com indicação do método de assinatura utilizado

![Registro de Assinatura Facial](../../../assets/images/registro-assinatura-facial.png)

## Situações Especiais

### Falha no Reconhecimento

Se o sistema não conseguir reconhecer o colaborador após múltiplas tentativas:

1. Verifique as condições de iluminação e posicionamento
2. Confira se o colaborador é realmente quem deveria estar assinando
3. Verifique se houve mudanças significativas na aparência desde o cadastro facial
4. Como alternativa, utilize a [Assinatura Digital Simples](./assinatura-digital.md)
5. Considere atualizar o cadastro facial posteriormente

### Indisponibilidade Temporária do Sistema de Reconhecimento

Em casos de problemas com o serviço de reconhecimento facial:

1. O sistema notificará automaticamente a indisponibilidade
2. Será oferecida a opção de utilizar a assinatura digital simples
3. Um alerta será registrado para verificação posterior pela equipe técnica

## Conformidade e Privacidade

O Sistema GNRX implementa as seguintes medidas para garantir conformidade legal e privacidade:

- Armazenamento criptografado de dados biométricos
- Uso exclusivo para fins de validação de entregas de EPIs
- Conformidade com LGPD (Lei Geral de Proteção de Dados)
- Exclusão segura dos dados biométricos mediante solicitação ou desligamento
- Consentimento explícito do colaborador para o processamento biométrico

## Melhores Práticas

- Realize o cadastro facial em condições semelhantes às que serão encontradas durante a entrega
- Atualize o cadastro facial periodicamente ou após mudanças significativas na aparência
- Utilize equipamentos com câmeras de boa qualidade para maior precisão
- Mantenha ambiente bem iluminado durante o processo de verificação
- Realize um teste de reconhecimento logo após o cadastro inicial para confirmar o funcionamento correto