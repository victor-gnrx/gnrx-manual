# Acessar Ficha

Esta página explica como acessar e gerar a Ficha EPI Digital dos colaboradores no Sistema GNRX Gestão de EPI.

## Visão Geral

A Ficha EPI Digital é um documento que registra o histórico de EPIs entregues ao colaborador, substituindo a tradicional ficha de papel. Contém as informações do colaborador, os EPIs recebidos, datas de entrega e devolução, além das assinaturas digitais ou por reconhecimento facial, atendendo aos requisitos da NR-6.

## Acessando a Ficha EPI

Para acessar a Ficha EPI de um colaborador:

1. No menu lateral, clique em **Estruturas**
2. Selecione **Colaboradores**
3. Localize e clique no colaborador desejado
4. Na parte superior direita da tela, clique no botão **Ficha EPI**

## Gerando uma Nova Ficha EPI

Ao clicar no botão **Ficha EPI**, o sistema exibirá um modal com opções:

![Modal Gerar Ficha](../../assets/images/modal-gerar-ficha.png)

1. Marque a opção **Exibir hash de verificação** para incluir o código de autenticidade
   - O hash é um código único que garante a autenticidade das assinaturas digitais presentes na ficha
   - Como descrito na imagem: "O hash de verificação é um código único que garante a autenticidade das assinaturas digitais presentes na ficha"

2. Clique no botão **Gerar Ficha** para processar e baixar o documento em PDF

## Conteúdo da Ficha EPI

Com base na imagem do Termo de Responsabilidade, a ficha contém:

- **Cabeçalho**: "TERMO DE RESPONSABILIDADE DE RECEBIMENTO E USO DE EPI"
- **Dados do Colaborador**: ID, nome, CPF, cargo, matrícula, turno, setor, situação
- **Datas**: Início de atividade, fim de atividade (quando aplicável)
- **Declaração de Responsabilidade**: Texto legal sobre o recebimento e uso dos EPIs
- **Tabela de EPIs**: Com colunas para:
  - Data de emissão
  - Data de solicitação
  - Motivo da solicitacao (Siglas cadastradas no sistema)
  - Descrição do EPI (NR-6 ou Nome do CA)
  - Unidade
  - Número do CA
  - Entrega (E)
  - Data de entrega
  - Assinatura de entrega (digital ou reconhecimento facial) - Com hash de verificação (se habilitado)
  - Data de retorno/devolução
  - Status de devolução (D/P/Q) - (D = Devolvido, P = Perda, Q = Quebra)

## Assinaturas na Ficha

A ficha apresenta dois tipos de assinaturas visíveis na imagem:

1. **Assinatura Digital**: Representada por um traço manuscrito digital
2. **Reconhecimento Facial**: Representada pela imagem do rosto do colaborador com a data e hora da confirmação

## Validação da Autenticidade da Ficha

Para validar a autenticidade de uma ficha através do hash:

1. Acesse a URL: app.gnrx.com.br/empresa/epi/solicitacoes/validar-assinatura
2. Na página "Validar Assinatura de EPI", digite o código de verificação (hash) de 64 caracteres
3. Clique no botão **Verificar Assinatura**

![Validar Assinatura](../../assets/images/validar-assinatura.png)

O sistema verificará a autenticidade do documento e exibirá o resultado.

## Significado dos Códigos na Ficha

Da imagem do Termo de Responsabilidade, podemos identificar:

- **Motivos**: 
  - PER: Permanente
  - TR: Temporário

- **Status de Devolução**:
  - D: Devolvido
  - P: Perda
  - Q: Quebra

## Conformidade Legal

A Ficha EPI Digital atende aos requisitos legais especificados no texto que aparece no documento:

> "DECLARO ter recebido e ter sido treinado quanto ao uso correto do(s) Equipamento(s) de Proteção Individual - EPI's abaixo especificado(s), nos termos dos artigos 166 e 167 da CLT, com redação dada pela Lei Federal nº 6.514/77, objetivando a proteção de minha integridade física, bem como a manutenção da minha saúde, comprometendo-me a: Usar o EPI apenas para a finalidade a que se destina; Responsabilizar-me por sua guarda e conservação; Comunicar ao empregador qualquer alteração que o torne impróprio para uso; Cumprir as determinações do empregador sobre o uso adequado."

## Próximos Passos

Após gerar a Ficha EPI Digital, você pode:

- Salvá-la no seu dispositivo
- Imprimi-la quando necessário
- Compartilhá-la com os responsáveis pela gestão de segurança
- Utilizá-la em fiscalizações ou auditorias

---

*Última atualização: 18 de Maio de 2025*