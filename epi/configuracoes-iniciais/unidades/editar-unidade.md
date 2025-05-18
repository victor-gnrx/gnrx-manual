# Editar Unidade

Esta página explica como modificar as informações de uma unidade existente no Sistema GNRX Gestão de EPI.

## Visão Geral

A edição de unidades permite atualizar informações cadastrais, endereços e outros detalhes das localidades físicas da empresa registradas no sistema.

## Acessando a Tela de Edição

Existem duas formas de acessar a edição de uma unidade:

### Opção 1: A partir da Lista de Unidades

1. No menu lateral, clique em **Estruturas**
2. Selecione **Unidades**
3. Na lista de unidades, localize a unidade desejada
4. Clique no ícone de **Editar** (símbolo de lápis) na coluna de ações

![Acesso via Lista](../../../assets/images/editar-unidade-lista.png)

### Opção 2: A partir da Tela de Detalhes

1. Acesse a tela de detalhes da unidade (clicando em seu nome na lista)
2. Clique no botão **Atualizar** no canto superior direito da tela

![Botão Atualizar](../../../assets/images/botao-atualizar-unidade.png)

## Interface de Edição

A tela de edição apresenta o formulário preenchido com os dados atuais da unidade:

![Formulário de Edição](../../../assets/images/formulario-editar-unidade.png)

### Campos Editáveis

Todos os campos do cadastro podem ser atualizados:

| Campo | Descrição | Considerações ao Editar |
|-------|-----------|-------------------------|
| **Nome** | Nome da unidade | A alteração afetará todas as referências à unidade no sistema |
| **Endereço** | Logradouro e número | Atualize em caso de mudança física da unidade |
| **Bairro** | Bairro da unidade | Mantenha consistência com o CEP |
| **Cidade** | Cidade da unidade | Verifique a ortografia correta |
| **Estado** | UF da unidade | Utilize a abreviação padrão de dois caracteres |
| **CEP** | Código postal | Formato: 00000-000 |
| **Descrição** | Informações adicionais | Pode ser usado para registrar mudanças ou particularidades |
| **CNPJ** | Número do CNPJ | Mantenha a formatação padrão XX.XXX.XXX/XXXX-XX |
| **Quantidade de funcionários para multa** | Número oficial de colaboradores | Atualize conforme a variação no quadro de pessoal |
| **Latitude/Longitude** | Coordenadas geográficas | Importantes para funcionalidades de geolocalização |

## Processo de Edição

1. Modifique os campos necessários
2. Verifique cuidadosamente as alterações, especialmente em campos críticos como Nome e CNPJ
3. Clique no botão **Atualizar** para salvar as modificações
4. O sistema exibirá uma mensagem de confirmação após a atualização bem-sucedida

![Confirmação de Atualização](../../../assets/images/confirmacao-atualizacao-unidade.png)

## Impacto das Alterações

A edição de uma unidade pode ter os seguintes impactos no sistema:

- Alterações de nome afetam todos os relatórios e listagens
- Modificações no endereço impactam registros de entrega e logística
- Mudanças no CNPJ podem afetar documentos legais e fiscais
- Atualizações no número de funcionários podem influenciar cálculos de conformidade

## Histórico de Alterações

O sistema mantém um registro das modificações realizadas:

1. Na tela de detalhes da unidade, clique na aba **Visão Geral**
2. No painel de **Estatísticas**, verifique o campo **Última Atualização**
3. A data, hora e usuário responsável pela última modificação são exibidos

![Histórico de Atualizações](../../../assets/images/historico-atualizacao-unidade.png)

## Limitações e Restrições

Algumas limitações se aplicam à edição de unidades:

- Não é possível alterar o ID da unidade
- Se a unidade possui colaboradores ou setores vinculados, algumas alterações podem requerer aprovação adicional
- Unidades com status "Inativo" precisam ser reativadas antes da edição

## Melhores Práticas

Para edição eficiente de unidades:

- Mantenha uma nomenclatura consistente mesmo após alterações
- Documente o motivo das mudanças significativas no campo de descrição
- Informe os usuários do sistema sobre alterações no nome das unidades
- Verifique os relatórios após edições para garantir que estão refletindo corretamente as alterações
- Considere o impacto em integrações com outros sistemas antes de modificar campos-chave

## Próximos Passos

Após editar uma unidade, considere:

- Verificar os [setores vinculados](../setores/listar-setores.md) para garantir que estão corretos
- Atualizar [GHEs](../ghe/README.md) se as condições da unidade mudaram
- Revisar o cadastro de [colaboradores](../colaboradores/README.md) associados à unidade
- Atualizar configurações de estoque se necessário

---

*Última atualização: 16 de Maio de 2025*