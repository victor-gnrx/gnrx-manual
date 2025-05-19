# Adicionar Lote sem Variantes

Esta página explica como adicionar um novo lote de EPIs que não possuem variantes configuradas no Sistema GNRX Gestão de EPI.

## Visão Geral

Para itens que não possuem variantes configuradas (como tamanhos, cores ou outras características), o processo de adição de lote é simplificado, focando apenas na quantidade total e na distribuição por unidade.

![Adicionar Lote sem Variantes](../../../assets/images/adicionar-lote-sem-variantes.png)

## Processo Completo

O processo de adição de lote sem variantes é dividido em duas etapas principais:

### 1. Informações Básicas

Na primeira tela, você deve informar:

1. **Número do Lote**: Identificador único para o lote (ex: CA0001-L57)
   - Este código será usado para rastreabilidade de todos os itens do lote
   - Recomenda-se seguir um padrão como CA[Número do CA]-L[Sequencial]

2. **Quantidade Total**: Número total de unidades recebidas no lote
   - Esta quantidade será distribuída entre as unidades na próxima etapa

3. **Custo Unitário (R$)**: Valor de cada unidade para controle financeiro
   - O sistema calculará automaticamente o valor total do lote

Após preencher estes campos, clique em **Próximo Passo** para continuar.

### 2. Distribuição por Local

Na segunda tela, você distribuirá a quantidade total entre as unidades/locais:

1. **Seleção de Unidade**: Escolha a unidade no menu suspenso
   - As unidades disponíveis são aquelas cadastradas no sistema

2. **Informação de Quantidade**: Digite a quantidade a ser alocada para a unidade selecionada

3. **Adição de Distribuição**: Clique no botão **Adicionar** para confirmar

4. **Status da Distribuição**: O sistema mostrará:
   - "Total distribuído: X de Y"
   - "Disponível para distribuir: Z"

5. **Distribuição Existente**: As unidades já configuradas aparecem na lista abaixo com:
   - Nome da unidade
   - Quantidade alocada
   - Opções para editar ou remover

Após distribuir todas as unidades ou a quantidade desejada, clique em **Confirmar Entrada** para finalizar.

## Exemplo Prático

Para um lote de 430 protetores auditivos:

### Etapa 1: Informações Básicas
- Número do Lote: Digite **CA0001-L57**
- Quantidade Total: Digite **580**
- Custo Unitário: Digite o valor (ex: **R$ 15,00**)

### Etapa 2: Distribuição por Local
- Selecione a unidade **Belo Horizonte 2**
- Digite a quantidade **430**
- Clique em **Adicionar**
- O sistema mostra: "Total distribuído: 150 de 580" (supondo distribuição prévia)
- O sistema mostra: "Disponível para distribuir: 430"
- Na lista abaixo aparece **Belo Horizonte** com **150** unidades já alocadas

- Ao finalizar, clique em **Confirmar Entrada**

## Considerações Importantes

- **Não é obrigatório distribuir toda a quantidade**: É possível deixar parte do estoque sem alocação específica
- **Validações automáticas**: O sistema impede que você distribua mais unidades do que o total disponível
- **Edição posterior**: É possível ajustar a distribuição posteriormente através da função de edição de lote
- **Mensagens de validação**: O sistema alertará sobre possíveis erros como "O lote com o número informado já existe"

## Resultado Final

Após a confirmação da entrada:

1. O lote será adicionado ao estoque do item
2. Cada unidade receberá um número de série único
3. As quantidades serão distribuídas conforme configurado
4. O sistema registrará a data de recebimento automaticamente

## Próximos Passos

Após adicionar o lote com sucesso, você pode:

- [Visualizar os itens do lote](./visualizar-items-lote.md) para verificar as unidades individuais
- [Editar o lote](./editar-lote.md) se necessário fazer ajustes
- [Gerenciar a validade](./gerenciar-validade.md) para controlar os prazos de vencimento

---

*Última atualização: 18 de Maio de 2025*