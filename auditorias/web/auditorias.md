---
description: Como visualizar, filtrar e gerenciar suas auditorias no sistema GNRX
icon: magnifying-glass
---

# Minhas Auditorias

A seção "Minhas Auditorias" centraliza todas as auditorias do sistema, permitindo visualizar, filtrar, pesquisar e gerenciar auditorias de maneira eficiente.

![Visão geral da tela Minhas Auditorias](/images/minhas-auditorias-geral.png)

## Acesso e Visão Geral

Acesse "Minhas Auditorias" através do menu lateral para visualizar:

- Lista completa de auditorias
- Status de cada auditoria (Em Andamento, Concluída, Programada)
- Datas de início e conclusão
- Índice de conformidade
- Local e setor da auditoria
- Responsável pela auditoria

## Filtros Avançados

Utilize os filtros disponíveis para localizar auditorias específicas:

<div className="card my-4 p-4">
  <h3>Filtros Disponíveis</h3>
  <div className="grid grid-cols-2 gap-2 mt-2">
    <div>
      <strong>Por Estado</strong>
      <ul className="list-disc ml-6">
        <li>Em Andamento</li>
        <li>Concluída</li>
        <li>Programada</li>
      </ul>
    </div>
    <div>
      <strong>Por Tipo</strong>
      <ul className="list-disc ml-6">
        <li>Modelo NR</li>
        <li>Modelo Customizado</li>
      </ul>
    </div>
    <div>
      <strong>Por Período</strong>
      <ul className="list-disc ml-6">
        <li>Data de início</li>
        <li>Data de conclusão</li>
      </ul>
    </div>
    <div>
      <strong>Por Local</strong>
      <ul className="list-disc ml-6">
        <li>Local de trabalho</li>
        <li>Setor</li>
      </ul>
    </div>
  </div>
</div>

Além dos filtros predefinidos, você pode usar a barra de pesquisa para encontrar auditorias por:
- Código da auditoria
- Nome da auditoria
- Responsável
- Palavras-chave no conteúdo

## Detalhes da Auditoria

Para visualizar detalhes de uma auditoria específica:

1. Clique na linha da auditoria desejada
2. O sistema abrirá a visão detalhada com as seguintes abas:

![Detalhes da Auditoria](/images/detalhes-auditoria.png)

### Aba Informações Gerais

Mostra os dados principais da auditoria:
- Informações de cabeçalho
- Datas e horários
- Local e responsáveis
- Índice geral de conformidade
- Gráfico resumo por seção

### Aba Itens

Lista todos os itens do checklist com:
- Status de conformidade de cada item
- Evidências anexadas (fotos)
- Observações registradas
- Ações corretivas sugeridas

### Aba Fotos

Galeria de todas as fotos registradas durante a auditoria:
- Visualização em miniatura
- Opção de ampliação
- Identificação do item relacionado
- Data e hora do registro

### Aba Planos de Ação

Exibe os planos de ação relacionados à auditoria:
- Planos em andamento
- Planos concluídos
- Opção para criar novo plano de ação

## Ações Disponíveis

Dependendo do status da auditoria, diferentes ações estão disponíveis:

### Para Auditorias Em Andamento
- **Continuar Auditoria**: Retoma o preenchimento do checklist
- **Finalizar Auditoria**: Conclui a auditoria impedindo novas alterações

### Para Auditorias Concluídas
- **Visualizar Relatório**: Gera relatório detalhado
- **Criar Plano de Ação**: Inicia processo de tratamento de não conformidades
- **Exportar**: Salva a auditoria em formato PDF ou Excel

### Para Todas as Auditorias
- **Duplicar**: Cria uma nova auditoria com os mesmos parâmetros
- **Compartilhar**: Envia link da auditoria por email
- **Arquivar**: Move a auditoria para o histórico

## Origem das Auditorias

O sistema identifica a origem da auditoria com ícones específicos:

- 💻 Auditorias criadas via sistema web
- 📱 Auditorias realizadas via aplicativo mobile
- 🔄 Auditorias importadas de outros sistemas

## Comparação de Auditorias

A função de comparação permite analisar duas ou mais auditorias lado a lado:

1. Selecione as auditorias desejadas usando as caixas de seleção
2. Clique no botão **"Comparar Selecionados"**
3. Visualize as diferenças de conformidade item a item

![Comparação de Auditorias](/images/comparacao-auditorias.png)

## Exportação em Lote

Para exportar várias auditorias de uma só vez:

1. Selecione as auditorias desejadas
2. Clique em **"Exportar Selecionados"**
3. Escolha o formato (PDF, Excel)
4. Configure opções adicionais (incluir fotos, observações)
5. Confirme a exportação

## Dicas de Utilização

- 💡 **Dica 1**: Salve filtros frequentes como favoritos para acesso rápido
- 💡 **Dica 2**: Use a ordenação por colunas para facilitar a análise
- 💡 **Dica 3**: Configure notificações para receber alertas de auditorias pendentes

## Próximos Passos

- [Criar uma nova auditoria](/auditorias/web/nova-auditoria.md)
- [Emitir planos de ação](/auditorias/web/criar-planos-acao.md)
- [Verificar relatórios](/auditorias/web/visualizar-relatorios.md)