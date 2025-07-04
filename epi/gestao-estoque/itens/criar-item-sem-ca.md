# Criar Item sem CA

Esta página explica como cadastrar um novo item sem Certificado de Aprovação (CA) no Sistema GNRX Gestão de EPI.

## Visão Geral

Além dos EPIs certificados, o Sistema GNRX permite o cadastro de itens complementares que não possuem CA, como uniformes, calçados não certificados e acessórios. Estes itens, embora não sejam EPIs regulamentados pela NR-6, fazem parte do gerenciamento completo de equipamentos fornecidos aos colaboradores.

<figure><img src="../../.gitbook/assets/image (30).png" alt="" width="373"><figcaption><p>Criar item sem CA</p></figcaption></figure>

## Quando Utilizar esta Opção

O cadastro de itens sem CA é adequado para:

* Uniformes e vestimentas profissionais (camisas, calças, jalecos)
* Acessórios complementares não certificados
* Itens importados sem certificação brasileira
* Equipamentos de uso pessoal não classificados como EPIs

## Acessando o Formulário

Para criar um novo item sem CA:

1. No menu lateral, clique em **Inventário**
2. Selecione **Inventário de Items**
3. Clique no botão **Novo Item** no canto superior direito da tela

## Preenchendo o Formulário

O modal "Criar Item" será exibido com os seguintes campos:

### 1. Informações Básicas

* **Nome**: Digite o nome completo do item (ex: "Uniforme - Calça")
* **Número CA**: Mantenha o toggle (botão de alternância) desativado
  * Este é o diferencial entre itens com e sem CA
  * Quando desativado, o campo de CA e validade ficará indisponível

### 2. Classificação do Item (Opcional)

* **EPI (NR-6)**: Você pode deixar este campo sem seleção ou selecionar a categoria mais próxima
  * Para uniformes, não é necessário selecionar uma categoria específica
  * A seleção não tem impacto regulatório para itens sem CA

### 3. Período de Troca (Opcional)

* **Tempo de Troca (Dias)**: Este campo pode ser deixado desativado para itens sem período definido
  * Para uniformes com trocas programadas, ative o toggle e defina um valor
  * Exemplo: "180" para uniformes trocados semestralmente

### 4. Informações do Fabricante e Complementares

* **Fabricante**:Selecione o fabricante (ex: "GNRx")
* **Descrição (Opcional)**: Utilize este campo para informações complementares como:
  * Características específicas
  * Material de fabricação
  * Finalidade de uso
  * Requisitos especiais

## Salvando o Cadastro

Após preencher os campos desejados:

1. Verifique se as informações estão corretas
2. Clique no botão **Salvar** no canto inferior direito do modal
3. O sistema processará o cadastro e exibirá uma mensagem de confirmação
4. O novo item será adicionado à lista com indicação "N/A" nos campos de CA e validade

## Particularidades de Itens sem CA

O sistema trata itens sem CA de maneira específica:

* Os campos de CA e validade exibirão "N/A" na listagem
* Não haverá avisos ou alertas de vencimento de CA
* O controle de estoque funciona normalmente
* É possível criar variantes (tamanhos, cores, etc.)
* A rastreabilidade permanece ativa, com número de série para cada item

## Exemplos de Itens sem CA na Listagem

Na lista de itens, você pode identificar os cadastros sem CA por:

* "N/A" no campo CA
* "N/A" no campo Validade
* Geralmente possuem "0 dias" no campo Tempo de Troca (a menos que configurado diferente)

## Limitações Regulatórias

É importante compreender que:

* Itens sem CA não são considerados EPIs oficiais perante a legislação
* Não são suficientes para atender requisitos legais de proteção
* Não substituem EPIs certificados em funções de risco
* Servem como complemento aos EPIs certificados

## Adicionando ao Estoque

Após o cadastro do item sem CA:

1. [Adicione variantes](../variantes/configurar-tipos-variante.md) se necessário (tamanhos, cores)
2. [Cadastre um lote](../lotes/adicionar-lote.md) para registrar a entrada no estoque
3. Defina as quantidades disponíveis para cada variante

## Controle Simplificado

Para itens sem CA, o sistema permite um controle mais simplificado:

* Período de troca opcional
* Sem verificação de conformidade com normas
* Possibilidade de cadastro simplificado de lotes
* Flexibilidade na definição de características

## Próximos Passos

Após cadastrar um item sem CA com sucesso, você pode:

1. [Configurar tipos de variante](../variantes/configurar-tipos-variante.md) como tamanho, cor, etc.
2. [Cadastrar valores para as variantes](../variantes/adicionar-valores-variante.md)
3. [Adicionar estoque](../lotes/adicionar-lote.md) para o novo item
4. Verificar o [item na listagem](listar-itens.md) para confirmar o cadastro

***

_Última atualização: 18 de Maio de 2025_
