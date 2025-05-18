# Criar GHE

Esta página explica como adicionar um novo Grupo Homogêneo de Exposição (GHE) no Sistema GNRX Gestão de EPI.

## Visão Geral

A criação de um GHE é fundamental para a correta atribuição de Equipamentos de Proteção Individual, pois estabelece a relação entre os riscos ocupacionais e os EPIs necessários para um grupo específico de colaboradores.

## Acessando a Tela de Criação

Para iniciar o cadastro de um novo GHE:

1. No menu lateral, clique em **Estruturas**
2. Selecione **GHEs**
3. Na tela de listagem, clique no botão **Novo GHE** no canto superior direito

![Botão Novo GHE](../../../assets/images/botao-novo-ghe.png)

## Formulário de Cadastro

Ao clicar em "Novo GHE", o sistema exibirá um modal com o formulário de criação:

![Formulário Novo GHE](../../../assets/images/formulario-novo-ghe.png)

### Campos do Formulário

| Campo | Descrição | Obrigatoriedade | Exemplo |
|-------|-----------|-----------------|---------|
| **Nome** | Identificação do GHE | Obrigatório | "Operadores de Empilhadeira" |
| **Unidade** | Unidade física onde o GHE existe | Obrigatório | "Belo Horizonte" |
| **Descrição** | Detalhamento das atividades ou características do grupo | Opcional | "Colaboradores que operam equipamentos de movimentação de carga" |
| **Medidas de Controle** | Medidas gerais adotadas para controle dos riscos | Opcional | "Treinamento específico, manutenção preventiva dos equipamentos" |

## Preenchendo o Formulário

1. Digite o **Nome** do GHE
   - Use nomes descritivos que identifiquem claramente o grupo
   - Mantenha consistência com a nomenclatura utilizada em documentos de SST
   - Considere incluir a função ou atividade principal no nome

2. Selecione a **Unidade**
   - Escolha a unidade física onde este GHE está presente
   - Um mesmo conceito de GHE pode ser replicado em diferentes unidades
   - Cada unidade terá seu próprio registro de GHE, mesmo com nomes idênticos

3. Adicione uma **Descrição** (opcional)
   - Detalhe as atividades realizadas pelo grupo
   - Inclua informações sobre o ambiente de trabalho
   - Mencione particularidades relevantes para a exposição a riscos

4. Informe as **Medidas de Controle** (opcional)
   - Descreva medidas administrativas ou coletivas já implementadas
   - Registre procedimentos de segurança específicos
   - Mencione controles de engenharia existentes

5. Revise as informações inseridas

6. Clique no botão **Salvar** para criar o GHE

## Após a Criação

Quando um novo GHE é criado com sucesso:

1. O sistema exibe uma mensagem de confirmação
2. O GHE é adicionado à lista de grupos
3. Você é redirecionado para a tela de detalhes do GHE recém-criado

![Confirmação de Criação](../../../assets/images/confirmacao-criacao-ghe.png)

## Próximas Etapas Obrigatórias

Após criar um GHE, é essencial completar a configuração com:

### 1. Vinculação de Riscos Ocupacionais

O próximo passo fundamental é associar os riscos ocupacionais específicos ao GHE:

1. Na tela de detalhes do GHE, selecione a aba **Riscos / EPIs**
2. Clique no botão **Editar**
3. Selecione os riscos ocupacionais aplicáveis a este grupo
4. Salve as alterações

> **Importante:** Um GHE sem riscos associados não cumpre sua função no sistema. A associação de riscos é obrigatória para a correta gestão de EPIs.

### 2. Vinculação de EPIs

Após associar os riscos, é necessário verificar e confirmar os EPIs recomendados:

1. Para cada risco selecionado, clique no botão **Ver EPIs**
2. Verifique os EPIs automaticamente sugeridos
3. Adicione ou remova EPIs conforme necessário
4. Salve as alterações

Para instruções detalhadas sobre estas etapas, consulte:
- [Vincular Riscos](./vincular-riscos.md)
- [Vincular EPIs](./vincular-epis.md)

## Considerações Importantes

- A criação de um GHE deve ser baseada em avaliações técnicas de riscos (PGR/PPRA)
- O GHE só será efetivo após a vinculação de riscos e EPIs
- Um mesmo colaborador pode pertencer a mais de um GHE, dependendo de suas atividades
- Recomenda-se consultar os profissionais de SST da empresa para definição adequada dos grupos

## Melhores Práticas

- **Alinhamento com SST**: Crie GHEs consistentes com os documentos técnicos de segurança do trabalho
- **Nomenclatura Clara**: Adote nomes que identifiquem facilmente a função ou exposição do grupo
- **Granularidade Adequada**: Evite GHEs muito genéricos ou excessivamente específicos
- **Documentação**: Mantenha registros dos critérios utilizados para definição de cada GHE
- **Revisão Periódica**: Atualize os GHEs sempre que houver mudanças nos processos ou condições de trabalho

## Erros Comuns e Soluções

| Erro | Solução |
|------|---------|
| "Nome já existe para esta unidade" | Escolha um nome único ou mais específico para o GHE nesta unidade |
| "Unidade não encontrada" | Verifique se a unidade foi previamente cadastrada no sistema |
| "Erro ao salvar" | Verifique se todos os campos obrigatórios foram preenchidos corretamente |

---

*Última atualização: 16 de Maio de 2025*