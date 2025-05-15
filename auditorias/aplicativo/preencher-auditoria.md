---
description: Preenchendo itens no checklist de auditoria
icon: check-square
---

# Como Preencher uma Auditoria

Este guia explica como realizar o preenchimento de itens em uma auditoria no aplicativo GNRX Auditorias, desde a navegação pelas seções até a avaliação de conformidade dos itens.

## Visão Geral da Tela de Detalhes Auditoria
Após criar uma auditoria, e selecionar a auditoria/checklist criada, você verá a tela inicial do checklist com os seguintes elementos:

<div style="text-align: center; margin: 20px 0;">
  <img src="https://example.com/imagens/app-preenchimento.png" alt="Tela de preenchimento de auditoria" width="300" />
</div>

1. **Barra Superior**: No lado esquerdo, temos quantos itens foram preenchidos Ex: 0 de 33 itens preenchidos
2. **Barra Superior**: No lado direito, temos o um botão de recarregar a auditoria.
3. **Nome da Auditoria**: Exibe o nome da auditoria, com o número único da auditoria criada. Só aparece se a auditoria tiver sido sincronizada.
4. **Informações Adicionais**: Exibe informações adicionais sobre a auditoria, como data de criação, unidade e informações adicionais do modelo.
5. **Localização**: Permite você obter a localização atual da auditoria, via GPS.
6. **Botão de Iniciar Auditoria**: Permite iniciar a auditoria e ir para a tela de preenchimento.
7. **Botão de Editar Auditoria**: Permite editar a auditoria, como nome, descrição, unidade e setor.
8. **Excluir Auditoria**: Permite excluir a auditoria.
9. **Assinatura**: Permite coletar assinaturas digitais.
10. **Botão Gerar Relatório**: Permite gerar um relatório para a auditoria.

### Obtendo Localização

Para obter a localização atual da auditoria, basta seguir os passos abaixo:

1. Vá na seção de Localização.
2. Se tiver "Localização não definida", é que você ainda não definiu a localização da auditoria.
3. Para definir a localização da auditoria, basta clicar no botão "Obter GPS".
4. Após clicar no botão, o aplicativo irá pedir permissão para acessar a localização do dispositivo.
5. Se a permissão for dada, o aplicativo informar que está obtendo a localização atual.
   - Este processo pode demorar alguns segundos.
6. Após obter a localização, o aplicativo irá atualizar a localização na seção de Localização, com a latitude e longitude.
7. Para atualizar a localização, basta clicar no botão "Atualizar GPS".

### Coletando Assinaturas

Para coletar assinaturas digitais, basta seguir os passos abaixo:

1. Vá na seção de Assinatura.
2. Para coletar uma assinatura, clique no botão "Incluir Assinatura".
3. Será aberto uma nova tela para preenchimento.
4. Preencha o nome completo do assinante.
5. Efetue a assinatura desenhando na tela.
   - Caso tenha erros na assinatura, clique em "Limpar" e tente novamente.
6. Após a assinatura ser feita, clique em "Confirmar".
7. Você pode adicionar mais assinaturas digitais clicando no botão "Incluir Assinatura".
8. Caso queria excluir uma assinatura, clique no botão "Excluir Assinatura".
9. Caso a assinatura já tenha sido sincronizada, não será mais possível excluir.

### Excluindo uma Auditoria

Para excluir uma auditoria, basta seguir os passos abaixo:

1. Vá na seção de Ações.
2. Clique no botão "Excluir".
3. Abrirá uma tela para confirmação.
4. Clique em "Excluir" para confirmar a exclusão.
   - Caso a auditoria não tenha sido sincronizada, todas as informações serão excluídas permanentemente.
   - Caso a auditoria tenha sido sincronizada, todas as informações serão excluídas no dispositivo, mas não no sistema web.

## Preenchendo a auditoria

Para inciar o preenchimento, na tela de "Detalhes Auditoria", clique no botão "Iniciar Auditoria", localizado na seção de Ações.

Após clicar no botão, o aplicativo irá abrir a tela de preenchimento do checklist.

## Tipos de Itens

Na auditoria, existem diversos tipos de itens, são eles:

### Conformidade

Este é o tipo de item mais comum, onde você deverá avaliar a conformidade de cada item do checklist.
O preenchimento funciona da seguinte forma:

No quadrado onde está uma "?" você pode clicar para ir alternando entre as opções de conformidade:
   
   - **Conforme** (C) (Verde): O item atende completamente aos requisitos
   - **Não Conforme** (N/C) (Vermelho): O item não atende aos requisitos. Abre uma nova opção de conformidade, o resolvido:
     - **Resolvido** (OK) (Verde): O item foi resolvido
     - **Alíneas não conformes**: Com no Não conforme, aparece-rá a opção de definir quais alíneas estão não conformes
   - **Não Aplicável** (N/A) (Cinza): O item não se aplica à situação atual
   - **Não Avaliado** (?) (Branco): O item não foi verificado nesta auditoria

<div style="text-align: center; margin: 20px 0;">
  <img src="https://example.com/imagens/app-opcoes-conformidade.png" alt="Opções de conformidade" width="300" />
</div>

### Peso / Nota

Este item é um tipo especial, onde você pode definir uma nota numérica para seu item.

Aparecerá os números de notas disponíveis no item, e você pode clicar no número para definir a nota:

<div style="text-align: center; margin: 20px 0;">
  <img src="https://example.com/imagens/app-nota.png" alt="Nota" width="300" />
</div>

### Informação

Este item é apenas um texto, onde o responsável pela criação do modelo deixou alguma informação relevante sobre a auditoria.

<div style="text-align: center; margin: 20px 0;">
  <img src="https://example.com/imagens/app-informacao.png" alt="Informação" width="300" />
</div>

### Texto

Este item é um texto, onde você pode preencher o texto que deseja, sem restrições.

<div style="text-align: center; margin: 20px 0;">
  <img src="https://example.com/imagens/app-texto.png" alt="Texto" width="300" />
</div>

### Número

Este item é para preenchimento apenas de números.

<div style="text-align: center; margin: 20px 0;">
  <img src="https://example.com/imagens/app-numero.png" alt="Número" width="300" />
</div>

### Temperatura

Este item é para preenchimento de números com uma escala de temperatura.
O preenchimento dele será automaticamente formatado como ºC.

<div style="text-align: center; margin: 20px 0;">
  <img src="https://example.com/imagens/app-temperatura.png" alt="Temperatura" width="300" />
</div>

### Data

Este item é para preenchimento de datas.
Nele, clicando no calendário, você pode escolher a data que deseja.

<div style="text-align: center; margin: 20px 0;">
  <img src="https://example.com/imagens/app-data.png" alt="Data" width="300" />
</div>

### Hora

Este item é para preenchimento de datas.
Nele, clicando no relógio, você pode escolher a hora que deseja.

<div style="text-align: center; margin: 20px 0;">
  <img src="https://example.com/imagens/app-hora.png" alt="Hora" width="300" />
</div>


## Continuando uma Auditoria em Andamento

Para retomar o preenchimento de uma auditoria salva:

1. Na tela inicial, acesse "Minhas Auditorias"
2. Toque na auditoria para abri-la
3. O aplicativo informará que a auditoria ainda tem itens por preencher.
4. Continue o preenchimento de onde parou

## Dicas para um Preenchimento Eficiente

- **Prepare-se antes**: Familiarize-se com o modelo de checklist antes de iniciar a auditoria
- **Siga uma sequência lógica**: Complete uma seção por vez, na ordem apresentada
- **Documente adequadamente**: Adicione fotos e observações detalhadas, especialmente para não conformidades
- **Salve regularmente**: Evite perda de trabalho salvando seu progresso frequentemente
- **Priorize itens críticos**: Em auditorias extensas, comece pelos itens de maior impacto
- **Trabalhe offline conscientemente**: Lembre-se de sincronizar assim que houver conexão disponível

## Solução de Problemas Comuns

### Tela congelando durante o preenchimento
- Dispositivos com pouca memória podem apresentar lentidão
- Feche outros aplicativos em execução
- Reinicie o aplicativo ou o dispositivo

## Próximos Passos

Após preencher os itens do checklist, você pode complementar com evidências fotográficas e observações:

- [Como Tirar Fotos e Anexar Evidências](tirar-fotos.md)
- [Como Adicionar Observações](adicionar-observacoes.md)
- [Finalizando e Enviando a Auditoria](finalizar-enviar.md)