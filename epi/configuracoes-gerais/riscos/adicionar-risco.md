---
icon: burst
---

# Adicionar Risco

## Introdução

A funcionalidade de adicionar novo risco permite criar registros personalizados de riscos ocupacionais específicos para a realidade da empresa. Esta capacidade é essencial para complementar os riscos pré-configurados do sistema, adaptando o GNRX às particularidades dos ambientes e processos de trabalho da organização.

<figure><img src="../../.gitbook/assets/image (59).png" alt=""><figcaption></figcaption></figure>

## Como Acessar

Para adicionar um novo risco ocupacional:

1. Acesse o menu **Configurações** na barra de navegação principal
2. Selecione a opção **Riscos** no submenu que se abre
3. Clique no botão **Criar Novo Risco** no canto superior direito da tela

## Formulário de Criação de Risco

O modal de criação de risco apresenta os seguintes campos:

### Campos Obrigatórios

* **Nome**: Denominação clara e objetiva do risco
  * _Exemplo: "Exposição a solventes orgânicos" ou "Trabalho em espaços confinados"_
  * Campo de texto com limite de 100 caracteres
  * Deve ser único no sistema (não pode haver dois riscos com o mesmo nome)
* **Descrição**: Detalhamento sobre o risco, suas características e potenciais consequências
  * _Exemplo: "Contato com solventes que podem causar irritação na pele e vias respiratórias"_
  * Campo de texto com limite de 500 caracteres
  * Deve ser informativo e específico para orientar medidas de proteção
* **Categoria**: Classificação do risco conforme sua natureza
  * Campo de seleção com as seguintes opções:
    * Riscos físicos
    * Riscos químicos
    * Riscos biológicos
    * Riscos ergonômicos
    * Riscos de acidentes
  * Determinará como o risco será agrupado no sistema

### Botões de Ação

* **Salvar**: Confirma a criação do novo risco e adiciona-o à base de dados
* **Cancelar**: Fecha o modal sem salvar as informações, descartando o novo risco

## Passo a Passo para Adicionar um Risco

### 1. Preparação

Antes de criar um novo risco, verifique se:

* O risco ainda não existe na base pré-configurada ou nos riscos personalizados
* Você tem clareza sobre a categoria mais adequada para classificá-lo
* Você possui informações suficientes para descrever o risco com precisão

### 2. Preenchimento do Formulário

1. Clique no botão **Criar Novo Risco**
2. No campo **Nome**, digite uma denominação clara e específica para o risco
3. No campo **Descrição**, forneça detalhes sobre o risco, suas características e efeitos potenciais
4. No campo **Categoria**, selecione a classificação mais adequada para o risco

### 3. Revisão e Confirmação

1. Verifique se todas as informações estão corretas e completas
2. Clique no botão **Salvar** para confirmar a criação do risco
3. Aguarde a mensagem de confirmação do sistema

### 4. Verificação

Após salvar, o novo risco será exibido na lista de riscos ocupacionais, pronto para ser:

* Associado a GHEs (Grupos Homogêneos de Exposição)
* Vinculado a EPIs apropriados
* Utilizado em documentações de saúde e segurança

## Boas Práticas

Para criar riscos eficazes e úteis, siga estas recomendações:

* **Seja específico**: Evite nomes genéricos como "Risco químico" (use "Exposição a ácido sulfúrico" em vez disso)
* **Use terminologia técnica**: Adote termos reconhecidos na área de saúde e segurança do trabalho
* **Forneça descrições completas**: Inclua informações sobre efeitos, circunstâncias e indicadores do risco
* **Mantenha a consistência**: Siga o mesmo padrão de nomenclatura usado nos riscos pré-configurados
* **Evite duplicidades**: Verifique se o risco já não existe com outro nome antes de criar um novo

## Considerações Técnicas

* **Unicidade**: O sistema não permitirá criar riscos com nomes idênticos
* **Caracteres especiais**: Evite o uso de caracteres especiais no nome do risco
* **Persistência**: Uma vez criado, o risco pode ser editado, mas não completamente excluído
* **Associações**: Ao criar um risco novo, será necessário configurar suas associações com EPIs adequados

## Próximos Passos

Após adicionar um novo risco, você pode:

* [Editar Risco](broken-reference) - Modificar as informações do risco recém-criado se necessário
* Associar o risco a GHEs específicos na seção de configuração de GHEs
* Vincular EPIs apropriados ao risco na seção de catálogo de EPIs

***

_Última atualização: 18 de Maio de 2025_
