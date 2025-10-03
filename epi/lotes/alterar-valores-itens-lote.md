---
icon: cart-plus
layout:
  width: default
  title:
    visible: true
  description:
    visible: true
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
  metadata:
    visible: true
---

# Alterar valores dos itens do lote

## Alterar Custo Unitário do Lote

Esta página explica como atualizar o valor de custo unitário de um lote já cadastrado no Sistema GNRx Gestão de EPI.

### Visão Geral

A funcionalidade de alteração de custo permite ajustar o valor unitário de todos os itens de um lote específico. Esta atualização afeta automaticamente:

* **Itens unitários do lote**: Todos os itens com número de série deste lote
* **Solicitações realizadas**: Solicitações que incluem itens deste lote
* **Relatórios financeiros**: Inventário, custos por setor e dashboards

### Quando Utilizar

* Correção de valores cadastrados incorretamente

### Como Alterar

#### 1. Acessar a Funcionalidade

1. Navegue até a página de detalhes do Item
2. Localize a seção **Lotes**
3. Na linha do lote desejado, clique no ícone **"Olho"** para visualizar detalhes.
4. Na telha de detalhes do lote, **coloque o mouse em cima da seção "Custo Total". Será exibido um ícone de editar no canto superior direito.**

<figure><img src="../.gitbook/assets/image (76).png" alt=""><figcaption></figcaption></figure>

#### 2. Preencher o Novo Valor

O diálogo exibe:

* **Custo Atual**: Valor atual cadastrado (apenas visualização)
*   **Novo Custo**: Digite o novo valor

    * Use vírgula para centavos (ex: 25,50)
    * Campo obrigatório
    * Use o botão "X" para limpar

    <figure><img src="../.gitbook/assets/image (75).png" alt="" width="382"><figcaption></figcaption></figure>

#### 3. Confirmar

1. Clique em **Atualizar Custo**
2. Aguarde o processamento
3. O sistema exibirá: "X itens e Y solicitações atualizadas"

### Exemplo Prático

**Cenário**: Correção de custo de R$ 8,00 para R$ 12,50

1. Acesse o item "Luva de Proteção Nitrílica"
2. Na seção de lotes, clique no ícone de edição do lote "CA0001-L42"
3. Digite **12,50** no campo Novo Custo
4. Clique em **Atualizar Custo**
5. Resultado: "150 itens e 32 solicitações atualizadas"

### Importantes

* **Permissão necessária**: Gestor ou Administrador

```rust
epis:gerenciar:estoque
```

* **Performance**: Lotes grandes podem levar alguns segundos para processar

### Validações

O sistema valida:

* Valor deve ser maior que zero
* Valor deve ser diferente do atual
* Formato monetário válido

***

_Última atualização: 3 de Outubro de 2025_
