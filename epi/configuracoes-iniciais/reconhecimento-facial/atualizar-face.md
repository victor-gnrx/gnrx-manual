# Atualizar Face

Esta página explica como atualizar o cadastro de reconhecimento facial de colaboradores no Sistema GNRX Gestão de EPI.

## Visão Geral

A atualização do reconhecimento facial é necessária em diversas situações, como mudanças significativas na aparência do colaborador, problemas recorrentes de reconhecimento ou atualizações periódicas para maior precisão. Este processo permite manter a eficiência e segurança do sistema de autenticação biométrica utilizado nas operações de entrega e devolução de EPIs.

![Atualização de Face](../../../assets/images/atualizar-face.png)

## Quando Atualizar o Cadastro Facial

A atualização do reconhecimento facial é recomendada nas seguintes situações:

- **Alterações físicas significativas** (crescimento ou remoção de barba, mudança radical no corte de cabelo, perda ou ganho significativo de peso)
- **Adição ou remoção de elementos faciais** (início ou término do uso de óculos de grau)
- **Falhas frequentes no reconhecimento** (mais de 3 tentativas necessárias para reconhecimento)
- **Atualização periódica recomendada** (a cada 12 meses, conforme política da empresa)
- **Após problemas técnicos** (após restauração de backup ou migração de dados)

## Identificando a Necessidade de Atualização

O sistema fornece indicadores para ajudar a identificar quando uma atualização é necessária:

- Status "Desatualizado" na ficha do colaborador
- Alertas automáticos para cadastros com mais de 12 meses
- Registro de múltiplas falhas de reconhecimento no log do sistema
- Feedback do colaborador sobre dificuldades recorrentes

## Processo de Atualização pela Web

### Acesso à Função de Atualização

1. No menu lateral, clique em **Estruturas**
2. Selecione **Colaboradores**
3. Localize e clique no colaborador desejado para abrir seus detalhes
4. Na seção de informações pessoais, localize o campo **Reconhecimento Facial Cadastrado**
5. Se exibir "Sim", clique no botão **Editar** ao lado

![Botão Editar](../../../assets/images/botao-editar-facial.png)

### Etapas da Atualização

1. **Revisão do Cadastro Atual**:
   - O sistema exibirá informações sobre o cadastro atual, incluindo data da última atualização
   - Você pode visualizar o nível de confiabilidade do cadastro atual (alto, médio, baixo)
   - Decida entre atualizar o cadastro existente ou realizar um novo cadastro completo

2. **Opções de Atualização**:
   - **Atualização Parcial**: Apenas complementa o cadastro existente com novas capturas
   - **Recadastro Completo**: Elimina o cadastro anterior e cria um novo (recomendado para mudanças significativas)
   - Selecione a opção mais adequada e clique em "Continuar"

3. **Captura das Novas Imagens**:
   - Siga as mesmas instruções do processo de cadastro inicial
   - Posicione o colaborador adequadamente e siga as orientações na tela
   - O sistema capturará as imagens necessárias de acordo com a opção selecionada

4. **Validação da Atualização**:
   - O sistema processará as novas imagens e atualizará o perfil biométrico
   - Uma mensagem de confirmação será exibida ao finalizar
   - O status e a data de atualização serão atualizados automaticamente

![Processo de Atualização](../../../assets/images/processo-atualizacao-facial.png)

## Atualização via Tablet ou Aplicativo Móvel

A atualização também pode ser realizada em dispositivos móveis:

1. Acesse o aplicativo GNRX Mobile
2. Faça login com credenciais de administrador ou gestor
3. Selecione **Colaboradores** no menu
4. Localize o colaborador e acesse seu perfil
5. Toque em **Reconhecimento Facial** e selecione **Atualizar**
6. Escolha entre atualização parcial ou recadastro completo
7. Siga as instruções na tela para completar o processo

Esta opção é especialmente útil para atualizações em campo ou em unidades remotas.

## Remoção e Recadastro

Em alguns casos, pode ser necessário remover completamente o cadastro facial e iniciá-lo novamente:

1. Na ficha do colaborador, localize o campo de reconhecimento facial
2. Clique no botão **Remover**
3. Confirme a ação no diálogo exibido
4. Após a remoção, o status voltará para "Não"
5. Clique em **Cadastrar** para iniciar um novo processo de cadastro

![Remover e Recadastrar](../../../assets/images/remover-recadastrar-facial.png)

## Verificação Após Atualização

Após a atualização, é fundamental testar o novo cadastro:

1. Solicite que o colaborador realize um teste de reconhecimento
2. Verifique se o sistema reconhece o colaborador em diferentes condições de iluminação
3. Confirme que o histórico de atualizações foi registrado corretamente
4. Solicite feedback do colaborador sobre a precisão do reconhecimento

## Histórico de Atualizações

O sistema mantém um registro completo de todas as atualizações:

1. Na ficha do colaborador, acesse a aba **Histórico**
2. Localize a seção **Reconhecimento Facial**
3. Visualize todas as atualizações, incluindo datas e responsáveis
4. Esta informação é valiosa para auditoria e rastreabilidade

## Resolução de Problemas

| Problema | Possível Causa | Solução |
|----------|----------------|---------|
| "Erro ao atualizar perfil" | Conflito com cadastro anterior | Remova completamente e realize um novo cadastro |
| "Perfil incompatível" | Mudança muito significativa | Opte pelo recadastro completo ao invés de atualização |
| "Falha ao sincronizar" | Problemas de conectividade | Verifique a conexão e tente novamente quando estável |
| "Qualidade insuficiente" | Condições inadequadas de captura | Melhore a iluminação e reposicione o colaborador |
| "Erro de permissão" | Acesso insuficiente | Verifique se o usuário possui permissões de administrador |

## Melhores Práticas

- Realize atualizações em ambiente com iluminação controlada
- Mantenha um cronograma regular de atualizações (a cada 6-12 meses)
- Documente os motivos das atualizações não programadas
- Treine os colaboradores sobre a importância de reportar problemas de reconhecimento
- Atualize imediatamente quando houver mudanças significativas na aparência
- Considere atualizações sazonais em ambientes com condições extremas (ex: trabalhadores que alternam entre ambiente interno e externo)

## Considerações de Desempenho

- A qualidade da atualização impacta diretamente a precisão do reconhecimento
- Atualizações frequentes sem necessidade podem sobrecarregar o sistema
- O recadastro completo utiliza mais recursos do sistema que atualizações parciais
- Atualizações em lote (vários colaboradores sequencialmente) podem ser mais eficientes

## Próximos Passos

Após a atualização bem-sucedida:

- Informe o colaborador sobre a conclusão do processo
- Solicite feedback após os primeiros usos do sistema atualizado
- Agende a próxima atualização periódica, se aplicável
- Documente quaisquer observações relevantes para futuras referências

Para outras operações relacionadas, consulte:

- [Cadastrar Face](./cadastrar-face.md) - Para colaboradores sem cadastro inicial
- [Testar Reconhecimento](./testar-reconhecimento.md) - Para validar o funcionamento
- [Solucionar Problemas](./solucionar-problemas.md) - Para dificuldades persistentes

---

*Última atualização: 18 de Maio de 2025*