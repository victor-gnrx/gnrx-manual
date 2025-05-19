# Visão Geral da Gestão de Motivos

## Introdução

O módulo de Gestão de Motivos permite configurar e gerenciar as justificativas utilizadas em diferentes operações relacionadas a Equipamentos de Proteção Individual (EPIs). Esta funcionalidade é essencial para padronizar as razões pelas quais EPIs são solicitados, devolvidos, perdidos ou quebrados, facilitando análises posteriores e garantindo consistência nos registros.

![Interface de Gestão de Motivos](../../../assets/images/gestao-motivos.png)

## Função e Importância

A gestão adequada dos motivos é fundamental para:

- **Organização**: Padronizar as justificativas utilizadas em todo o sistema
- **Análise de dados**: Facilitar a geração de relatórios e análises estatísticas
- **Auditoria**: Fornecer informações claras e consistentes para processos de auditoria
- **Rastreabilidade**: Permitir o acompanhamento detalhado do ciclo de vida dos EPIs
- **Conformidade**: Atender requisitos de documentação para conformidade com normas de segurança

## Categorias de Motivos

O sistema GNRX trabalha com quatro categorias principais de motivos:

### 1. Motivos de Solicitação

Justificativas para solicitar novos EPIs, como:
- Primeira solicitação (para colaboradores novos)
- Troca recorrente (substituição por desgaste normal)
- Perda (reposição por perda do equipamento anterior)
- Outros motivos específicos definidos pela empresa

### 2. Motivos de Devolução

Razões para a devolução de EPIs ao estoque, como:
- Devolução padrão (retorno normal após uso)
- Encerramento de atividade (colaborador não precisa mais do equipamento)
- Troca por outro modelo (substituição por EPI mais adequado)
- Outros motivos específicos definidos pela empresa

### 3. Motivos de Perda

Explicações para o registro de EPIs perdidos, como:
- Extravio (perda em local desconhecido)
- Roubo ou furto
- Perda em local de trabalho externo
- Outros motivos específicos definidos pela empresa

### 4. Motivos de Quebra

Justificativas para quebra ou dano em EPIs, como:
- Desgaste natural (após tempo de uso prolongado)
- Acidente (dano decorrente de incidente específico)
- Defeito de fabricação
- Outros motivos específicos definidos pela empresa

## Estrutura Comum dos Motivos

Cada motivo, independentemente da categoria, é composto por:

- **Motivo**: Nome descritivo da justificativa
- **Sigla**: Abreviação de até 4 caracteres para identificação rápida
- **Descrição (opcional)**: Detalhamento adicional sobre o motivo, quando necessário
- **Situação**: Status do motivo (Ativo ou Inativo)

## Interface e Navegação

A interface de Gestão de Motivos apresenta:

- **Navegação por abas**: Acesso rápido a cada categoria de motivo
- **Pesquisa**: Campo para localizar motivos específicos
- **Tabela de motivos**: Listagem dos motivos configurados, com opções de ordenação
- **Botão "Novo Motivo"**: Acesso à funcionalidade de criação de novos motivos

## Personalização e Padronização

O sistema GNRX oferece:

- **Motivos padrão**: Configurações iniciais com motivos comuns
- **Personalização**: Capacidade para adicionar, editar ou inativar motivos conforme necessidades específicas
- **Consistência**: Estrutura padronizada para todas as categorias de motivos

## Aplicação no Fluxo de Trabalho

Os motivos configurados são utilizados em diferentes pontos do sistema:

- **Criação de solicitações**: Seleção obrigatória do motivo ao solicitar EPIs
- **Registro de devoluções**: Definição do motivo ao devolver equipamentos
- **Documentação de perdas**: Justificativa ao registrar EPIs perdidos
- **Registro de quebras**: Explicação ao documentar equipamentos danificados

## Considerações Importantes

- A inativação de motivos não afeta registros históricos
- É recomendável manter a lista de motivos concisa e clara
- Motivos bem definidos auxiliam na análise de tendências e identificação de problemas

## Próximos Passos

Para utilizar efetivamente o módulo de Gestão de Motivos, consulte os seguintes guias detalhados:

- [Motivos de Solicitação](./motivos-solicitacao.md) - Como gerenciar as justificativas para solicitação de EPIs
- [Motivos de Devolução](./motivos-devolucao.md) - Como configurar os motivos para devolução de equipamentos
- [Motivos de Perda](./motivos-perda.md) - Como administrar as explicações para registro de EPIs perdidos
- [Motivos de Quebra](./motivos-quebra.md) - Como gerenciar as justificativas para quebra de equipamentos

---

*Última atualização: 18 de Maio de 2025*