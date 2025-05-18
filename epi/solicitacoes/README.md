# Solicitações

O módulo de Solicitações gerencia todo o fluxo de requisição, aprovação, entrega e devolução de Equipamentos de Proteção Individual (EPIs) no Sistema GNRX, garantindo o controle preciso e a conformidade legal de todo o processo.

## Visão Geral do Fluxo de Solicitações

O GNRX implementa um fluxo completo para gestão de EPIs, contemplando todas as etapas desde a solicitação inicial até a conclusão do ciclo de vida do equipamento:

![Fluxo de Solicitação de EPIs](../assets/images/fluxo-solicitacao-epi.png)

### 1. Solicitação
Criação da requisição de um ou mais EPIs para um colaborador específico, definindo motivos e detalhes.

### 2. Devolução de Pendentes (quando aplicável)
Caso existam itens pendentes de devolução, o sistema solicita a regularização antes da nova entrega.

### 3. Entrega
Separação e entrega física dos equipamentos solicitados, com registro detalhado no sistema.

### 4. Assinatura
Confirmação digital do recebimento pelo colaborador, com opções de assinatura digital e reconhecimento facial.

### 5. Ciclo de Vida
Acompanhamento do uso, incluindo eventuais devoluções, perdas, quebras ou substituições.

## Componentes do Módulo

### [Criar Solicitação](./criar-solicitacao/README.md)
Interface para registro de novas solicitações de EPIs, com seleção de colaborador, equipamentos, motivos e observações.

### [Devolução](./devolucao/README.md)
Gestão de itens pendentes de devolução, com opções para registrar devoluções, perdas ou quebras de equipamentos.

### [Entrega](./entrega/README.md)
Ferramentas para processar as entregas físicas dos EPIs solicitados, incluindo confirmação de itens e quantidades.

### [Assinatura](./assinatura/README.md)
Métodos seguros para documentar o recebimento dos EPIs pelos colaboradores, incluindo assinatura digital e reconhecimento facial.

## Principais Indicadores

O módulo de Solicitações fornece importantes indicadores para a gestão de EPIs:

- **Volume de solicitações** por período, unidade e setor
- **Tempo médio** entre solicitação e entrega
- **Taxa de conformidade** nas devoluções
- **Percentual de perdas e quebras** por tipo de EPI
- **Custos associados** à reposição não programada

## Benefícios do Processo Estruturado

- **Conformidade legal** com requisitos da NR-6 sobre entrega e registro de EPIs
- **Rastreabilidade completa** de todo o ciclo de vida dos equipamentos
- **Redução de perdas** através do controle efetivo de devoluções
- **Otimização de recursos** com entregas baseadas em necessidades reais
- **Evidência legal robusta** em caso de fiscalizações trabalhistas

## Integração com Outros Módulos

O módulo de Solicitações se integra diretamente com:

- **Gestão de Estoque**: Verificação de disponibilidade e baixa automática
- **Ficha de EPI Digital**: Atualização do histórico do colaborador
- **Reconhecimento Facial**: Assinatura segura por biometria facial
- **GHEs**: Validação automática de conformidade com riscos do colaborador