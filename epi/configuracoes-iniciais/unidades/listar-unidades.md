---
icon: house-building
---

# Listar Unidades

Esta página explica como acessar, visualizar e filtrar a lista de unidades cadastradas no Sistema GNRX Gestão de EPI.

## Acessando a Lista de Unidades

Para acessar a lista de unidades cadastradas no sistema:

1. No menu superior, clique em **Estruturas**
2. Selecione **Unidades**

<figure><img src="../../.gitbook/assets/image (6) (1) (1).png" alt=""><figcaption></figcaption></figure>

## Interface da Lista de Unidades

A tela de listagem de unidades apresenta uma visão consolidada de todas as unidades cadastradas no sistema, com as seguintes informações:

![Lista de Unidades](<../../.gitbook/assets/image (5) (1) (1).png>)

### Elementos da Interface

1. **Cabeçalho**:
   * **Total de unidades**: Contador do número de unidades no sistema
   * **Total Ativas:** Contador de número de unidades utilizáveis e em uso
   * **Unidades Inativas:** Que não estão em uso no sistema.
   * **Total de Colaboradores:** Quantidade Geral de colaboradores (Com duplicidades, caso esteja em 2 unidades)
   * **Total de Setores:** Contagem da quantidade de setores atribuidos nas unidades.
   * **Média:** Média de colaboradores por unidade.
2. **Barra de Pesquisa**:
   * Campo para busca de unidades por nome.
   * Botão "Pesquisar" para iniciar a busca
3. **Tabela de Unidades**:
   * **Nome**: Nome da unidade
   * **Endereço**: Localização física completa
   * **Descrição**: Informações adicionais sobre a unidade
   * **Colaboradores**: Total de colaboradores vinculados à unidade
   * **Setores**: Número de setores cadastrados na unidade
   * **Situação**: Estado atual (Ativo/Inativo)
   * **Criado em**: Data de criação do registro
   * **Opções**: Botões de ação (visualizar, editar, excluir)

## Funcionalidades Disponíveis

### Pesquisa e Filtros

Para localizar unidades específicas:

1. Digite um termo de busca no campo de pesquisa (nome)
2. Clique no botão **Pesquisar**
3. O sistema exibirá apenas as unidades que correspondem aos critérios de busca

> **Dica:** Para retornar à lista completa, limpe o campo de pesquisa e clique novamente em Pesquisar.

### Ações por Unidade

Para cada unidade na lista, você pode executar as seguintes ações através dos botões na coluna "Opções":

![Botões de Ação](<../../.gitbook/assets/image (7) (1) (1).png>)

* **Visualizar** (ícone de olho): Abre a tela de detalhes da unidade
* **Editar** (ícone de lápis): Abre o formulário para edição dos dados
* **Excluir/Desativar** (ícone de lixeira): Inicia o processo de desativação da unidade.

## Navegação para Detalhes

Para visualizar informações detalhadas de uma unidade específica:

1. Clique no nome da unidade na lista ou no ícone de visualização (olho)
2. O sistema abrirá a tela de detalhes da unidade, com abas para:
   * **Visão Geral**: Informações básicas
   * **Setores**: Lista de setores vinculados
   * **Colaboradores**: Funcionários associados
   * **GHEs**: Grupos Homogêneos de Exposição da unidade

<figure><img src="../../.gitbook/assets/image (9) (1) (1).png" alt=""><figcaption></figcaption></figure>



## Visualização de Situação

As unidades na lista são apresentadas com indicadores visuais de situação:

* **Ativo**: Exibido em verde, indica unidade em operação normal
* **Inativo**: Exibido em vermelho, indica unidade desativada

> **Nota:** Unidades inativas não aparecem em listas de seleção em outros módulos do sistema, mas mantêm seu histórico preservado.

## Solução de Problemas Comuns

| Problema                        | Solução                                                                                                      |
| ------------------------------- | ------------------------------------------------------------------------------------------------------------ |
| Lista de unidades vazia         | Verifique se você tem permissões para visualizar unidades ou se ainda não há unidades cadastradas no sistema |
| Pesquisa não retorna resultados | Tente termos mais genéricos ou verifique a ortografia                                                        |
| Unidade não pode ser excluída   | Verifique se há colaboradores, setores ou EPIs associados à unidade                                          |

## Próximos Passos

Após visualizar a lista de unidades, você pode:

* [Editar uma unidade existente](editar-unidade.md)
* [Desativar uma unidade](desativar-unidade.md)
* Configurar [setores](../setores/) para suas unidades
* Associar [colaboradores](../colaboradores/) às unidades

***

_Última atualização: 16 de Maio de 2025_
