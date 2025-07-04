---
icon: cart-plus
---

# Adicionar Lote Item Com Variantes

Esta página explica como adicionar um novo lote de EPIs que possuem variantes configuradas no Sistema GNRX Gestão de EPI.

## Visão Geral

Quando um item possui variantes (como tamanhos, cores ou outras características), o processo de adição de lote inclui etapas específicas para distribuir a quantidade total entre as diferentes combinações de variantes e unidades.

<figure><img src="../../.gitbook/assets/image (37).png" alt=""><figcaption><p>Adicionar Lote com Variantes</p></figcaption></figure>

## Processo Completo

O processo de adição de lote com variantes é dividido em três etapas principais:

### 1. Informações Básicas

Na primeira tela, você deve informar:

1. **Número do Lote**: Identificador único para o lote (ex: CA43350-L02)
   * Este código será usado para rastreabilidade de todos os itens do lote
   * Recomenda-se seguir um padrão como CA\[Número do CA]-L\[Sequencial]
2. **Quantidade Total**: Número total de unidades recebidas no lote
   * Esta quantidade será distribuída entre variantes e unidades nas próximas etapas
3. **Custo Unitário (R$)**: Valor de cada unidade para controle financeiro
   * O sistema calculará automaticamente o valor total do lote

Após preencher estes campos, clique em **Próximo Passo** para continuar.

### 2. Distribuição por Variantes

Na segunda tela, você distribuirá a quantidade total entre as variantes configuradas:

1. Para cada variante disponível (ex: Tamanho PP, P, M, G), informe:
   * **Quantidade**: Número de unidades para esta variante específica
2. Você pode adicionar mais combinações usando o botão **Adicionar Combinação**
   * Útil para casos em que há mais de um tipo de variante (tamanho + cor)
3. O sistema mostrará o **Status da Distribuição**:
   * "Total distribuído: X de Y" para acompanhar o progresso
   * Todas as unidades precisam ser distribuídas para prosseguir

Após distribuir todas as unidades, clique em **Próximo** para continuar.

### 3. Distribuição por Unidades

Na terceira tela, você distribuirá cada variante entre as unidades/locais:

1. O sistema mostrará cada variante separadamente (ex: "Tamanho: PP", "Tamanho: M")
2. Para cada variante, distribua as unidades entre os locais:
   * Insira a quantidade para cada unidade listada
   * O sistema mostrará o total de unidades daquela variante
3. Você pode deixar algumas unidades sem alocação específica usando a opção "Sem Unidade"
4. O status mostrará quando a distribuição estiver completa para cada variante

Após distribuir todas as variantes entre as unidades, clique em **Confirmar Entrada** para finalizar.

## Exemplo Prático

Para um lote de 50 uniformes com variantes de tamanho:

### Etapa 1: Informações Básicas

* Número do Lote: **CA124587-L002**
* Quantidade Total: **50**
* Custo Unitário: **R$ 15,20**
* Valor Total calculado: **R$ 760,00**

### Etapa 2: Distribuição por Variantes

* Tamanho PP: **25 unidades**
* Tamanho M: **25 unidades**
* Status: "Total distribuído: 50 de 50"

### Etapa 3: Distribuição por Unidades

Para Tamanho PP (total: 25 unidades):

* Belo Horizonte: **25 unidades**
* Status: "OK"

Para Tamanho M (total: 25 unidades):

* Belo Horizonte: **25 unidades**
* Status: "OK"

## Considerações Importantes

* **Todas as unidades devem ser distribuídas**: O sistema não permitirá avançar ou concluir o processo até que todas as unidades estejam distribuídas
* **Não é possível editar as variantes**: As variantes disponíveis são aquelas configuradas previamente para o item
* **Rastreabilidade individual**: Após a confirmação, o sistema gerará números de série individuais para cada unidade física
* **Mensagens de validação**: O sistema alertará sobre possíveis erros como "O lote com o número informado já existe"

## Resultado Final

Após a confirmação da entrada:

1. O lote será adicionado ao estoque do item
2. Cada unidade receberá um número de série único
3. As quantidades serão distribuídas conforme configurado
4. O sistema registrará a data de recebimento automaticamente

## Próximos Passos

Após adicionar o lote com sucesso, você pode:

* [Visualizar os itens do lote](visualizar-items-lote.md) para verificar as unidades individuais
* [Editar o lote](editar-lote.md) se necessário fazer ajustes
* [Gerenciar a validade](gerenciar-validade.md) para controlar os prazos de vencimento

***

_Última atualização: 18 de Maio de 2025_
