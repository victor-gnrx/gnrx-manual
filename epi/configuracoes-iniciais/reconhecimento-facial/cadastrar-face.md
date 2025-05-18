# Cadastrar Face

Esta página explica como realizar o cadastro de reconhecimento facial para colaboradores no Sistema GNRX Gestão de EPI.

## Visão Geral

O cadastro de reconhecimento facial é um processo simples que permite ao sistema identificar o colaborador de forma segura durante a assinatura de recebimento de EPIs, devoluções e outras operações que exigem autenticação. Este recurso elimina a necessidade de assinaturas físicas e garante que apenas o colaborador autorizado possa confirmar o recebimento de equipamentos.

![Cadastro de Face](../../../assets/images/cadastro-face.png)

## Pré-requisitos

Antes de iniciar o cadastro, verifique se:

1. O colaborador já está cadastrado no sistema
2. Você possui permissões de administrador ou gestor de EPIs
3. Está utilizando um dispositivo com câmera frontal de boa qualidade
4. O ambiente possui iluminação adequada (sem excesso de luz direta ou penumbra)
5. O colaborador está presente fisicamente para o cadastro

## Processo de Cadastro pela Web

### Acesso à Função de Cadastro

1. No menu lateral, clique em **Estruturas**
2. Selecione **Colaboradores**
3. Localize e clique no colaborador desejado para abrir seus detalhes
4. Na seção de informações pessoais, localize o campo **Reconhecimento Facial Cadastrado**
5. Se exibir "Não", clique no botão **Cadastrar** ao lado

![Botão Cadastrar](../../../assets/images/botao-cadastrar-facial.png)

### Etapas do Cadastro

1. **Preparação**:
   - Uma janela modal será aberta solicitando acesso à câmera
   - Autorize o acesso à câmera do dispositivo
   - Posicione o colaborador centralmente no enquadramento

2. **Captura das Imagens**:
   - O sistema solicitará que o colaborador posicione o rosto no contorno exibido
   - O processo capturará automaticamente múltiplos ângulos para maior precisão
   - Siga as instruções na tela para movimentar levemente a cabeça (olhar para cima, para os lados)
   - O sistema indicará o progresso do cadastro em percentual

3. **Validação**:
   - Após a captura completa, o sistema realizará uma verificação inicial
   - Se bem-sucedido, uma mensagem de confirmação será exibida
   - O status mudará automaticamente para "Sim" na ficha do colaborador

### Recomendações para Captura de Qualidade

Para garantir a melhor qualidade do cadastro facial:

- Certifique-se de que o rosto está bem iluminado, sem sombras fortes
- Remova óculos escuros (óculos de grau normais podem ser mantidos)
- Mantenha expressão neutra durante a captura
- Evite ambientes com fundo muito complexo ou em movimento
- Posicione a câmera na altura dos olhos do colaborador

## Cadastro via Tablet ou Aplicativo Móvel

O cadastro também pode ser realizado diretamente no tablet ou smartphone:

1. Acesse o aplicativo GNRX Mobile
2. Faça login com credenciais de administrador ou gestor
3. Selecione **Colaboradores** no menu
4. Localize o colaborador e acesse seu perfil
5. Toque em **Cadastrar Reconhecimento Facial**
6. Siga as instruções na tela para completar o processo

![Cadastro Mobile](../../../assets/images/cadastro-face-mobile.png)

Este método é especialmente útil para cadastros em campo ou em locais onde não há acesso direto ao sistema web.

## Verificação do Cadastro

Após concluir o cadastro, é recomendável realizar uma verificação:

1. Retorne à ficha do colaborador
2. Confirme que o status mudou para "Sim" no campo de reconhecimento facial
3. Opcionalmente, realize um teste de reconhecimento

![Confirmação de Cadastro](../../../assets/images/confirmacao-cadastro-facial.png)

## Solução de Problemas Comuns

| Problema | Possível Causa | Solução |
|----------|----------------|---------|
| "Erro ao acessar câmera" | Permissões de câmera bloqueadas | Verifique as configurações do navegador e autorize o acesso à câmera |
| "Iluminação insuficiente" | Ambiente muito escuro | Melhore a iluminação ou mude para um local mais claro |
| "Rosto não detectado" | Posicionamento incorreto | Reposicione o colaborador centralmente na câmera |
| "Falha na captura" | Movimentação excessiva | Peça ao colaborador para ficar mais estável durante a captura |
| "Erro de sincronização" | Problemas de conexão | Verifique a conexão com a internet e tente novamente |

## Considerações Importantes

- O cadastro facial é **opcional** mas altamente recomendado para maior segurança
- O colaborador deve concordar explicitamente com o cadastro facial
- Os dados biométricos são armazenados de forma segura e criptografada
- O cadastro deve ser renovado periodicamente (geralmente a cada 12 meses)
- Mudanças significativas na aparência (barba, corte de cabelo) podem exigir atualização

## Benefícios do Cadastro Facial

- Elimina a necessidade de assinaturas em papel
- Aumenta a segurança na entrega de EPIs
- Reduz fraudes e entregas não autorizadas
- Facilita auditorias e fiscalizações
- Otimiza o tempo de entrega e registro

## Próximos Passos

Após o cadastro bem-sucedido, o colaborador estará apto a:

- Receber EPIs com assinatura por reconhecimento facial
- Registrar devoluções de forma biométrica
- Acessar o aplicativo móvel via autenticação facial (quando configurado)

Se necessário, consulte também:

- [Atualizar Face](./atualizar-face.md) - Para renovação ou correção do cadastro
- [Testar Reconhecimento](./testar-reconhecimento.md) - Para validar o funcionamento
- [Solucionar Problemas](./solucionar-problemas.md) - Para casos de dificuldades persistentes

---

*Última atualização: 18 de Maio de 2025*