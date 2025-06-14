---
description: Sistema avançado de controle de acesso com roles e permissões granulares
icon: shield-check
---

# Sistema de Permissões e Roles

O sistema GNRX Auditorias utiliza um modelo avançado de controle de acesso baseado em **RBAC (Role-Based Access Control)** e **ABAC (Attribute-Based Access Control)**, oferecendo flexibilidade total para gerenciar quem pode fazer o quê, onde e quando no sistema.

{% hint style="info" %}
O sistema de roles e permissões substitui o antigo campo "tipo_usuario" por um modelo mais flexível e granular. Todos os usuários existentes foram automaticamente migrados para o novo sistema mantendo suas permissões atuais.
{% endhint %}

## Conceitos Fundamentais

### O que são Roles (Papéis)?

**Roles** são conjuntos de permissões agrupadas logicamente que definem o que um usuário pode fazer no sistema. Cada usuário pode ter uma ou mais roles atribuídas, e essas roles podem ser específicas para determinadas unidades ou setores.

### O que são Permissões?

**Permissões** são ações específicas que podem ser executadas no sistema, organizadas por:
- **Módulo**: Área do sistema (ex: auditorias, epis, formulários)
- **Ação**: O que pode ser feito (ex: criar, editar, visualizar, deletar)
- **Recurso**: Sobre o que a ação é executada (ex: auditoria, usuário, relatório)

### Controle Contextual (ABAC)

{% hint style="warning" %}
**Importante**: Apenas usuários com role "Administrador" podem gerenciar outros usuários e suas permissões. Esta é uma medida de segurança para evitar escalação não autorizada de privilégios.
{% endhint %}

Além das roles, o sistema considera:
- **Unidade de Trabalho**: Onde o usuário pode atuar
- **Setor**: Setor específico dentro da unidade
- **Hierarquia**: Relacionamento entre unidades e setores

## Roles Padrão do Sistema

O sistema inclui quatro roles pré-configuradas que atendem à maioria dos cenários organizacionais:

### 🟢 Operador
**Perfil**: Usuário básico que executa operações do dia a dia

**Principais Capacidades**:
- Criar e editar suas próprias auditorias
- Visualizar modelos de checklist (não pode criar)
- Solicitar EPIs para si mesmo
- Preencher formulários e registros
- Visualizar informações básicas de funcionários e estrutura
- Exportar relatórios de suas auditorias

**Limitações**:
- Não pode aprovar solicitações de EPIs
- Não pode gerenciar estoque
- Não pode criar modelos ou configurações
- Acesso restrito apenas às suas atividades

{% hint style="info" %}
**Ideal para**: Técnicos, auditores de campo, operadores de chão de fábrica que executam tarefas específicas sem responsabilidades de aprovação.
{% endhint %}

### 🟡 Supervisor
**Perfil**: Líder de equipe com responsabilidades de aprovação

**Principais Capacidades**:
- Todas as capacidades do Operador, mais:
- Finalizar auditorias de sua equipe
- Aprovar e rejeitar solicitações de EPIs
- Registrar entregas e devoluções de EPIs
- Editar dados de funcionários de sua supervisão
- Visualizar dashboards básicos
- Gerenciar atividades do seu setor/unidade

**Limitações**:
- Não pode criar modelos de formulários ou checklists
- Não pode gerenciar estoque geral
- Não pode ver todas as unidades da empresa

{% hint style="info" %}
**Ideal para**: Supervisores de equipe, encarregados de setor, líderes de turno que precisam aprovar solicitações e coordenar atividades operacionais.
{% endhint %}

### 🟠 Gestor
**Perfil**: Gerente com visão ampla dos processos

**Principais Capacidades**:
- Todas as capacidades do Supervisor, mais:
- Criar e editar modelos de checklist e formulários
- Gerenciar todos os aspectos de auditorias
- Visualizar e editar toda estrutura organizacional
- Gerar todos os tipos de relatórios
- Visualizar dados de múltiplas unidades
- Configurar GHEs, riscos ocupacionais e fabricantes

**Limitações**:
- Não pode gerenciar usuários
- Não pode alterar configurações críticas da empresa
- Não pode gerenciar estoque geral de EPIs

{% hint style="info" %}
**Ideal para**: Gerentes de área, coordenadores de segurança, analistas que precisam de visão ampla dos processos e capacidade de configuração.
{% endhint %}

### 🔴 Administrador
**Perfil**: Administrador com controle total do sistema

**Principais Capacidades**:
- Acesso completo a todas as funcionalidades
- Gerenciar usuários e suas permissões
- Configurar roles personalizadas
- Gerenciar estoque geral de EPIs
- Configurar integrações (WhatsApp, etc.)
- Editar configurações da empresa
- Acesso a todos os módulos e relatórios

{% hint style="warning" %}
**Atenção**: Role de Administrador deve ser concedida apenas a pessoas de absoluta confiança, pois tem acesso total ao sistema incluindo dados sensíveis e configurações críticas.
{% endhint %}

## Catálogo Completo de Permissões

Todas as permissões do sistema seguem o formato **módulo:ação:recurso** e estão organizadas por área funcional.

### 👥 MÓDULO: Usuários
| Permissão | Descrição | Operador | Supervisor | Gestor | Admin |
|-----------|-----------|----------|------------|--------|-------|
| `usuarios:criar:usuario` | Criar novos usuários no sistema | ❌ | ❌ | ❌ | ✅ |
| `usuarios:editar:usuario` | Editar informações de usuários existentes | ❌ | ❌ | ❌ | ✅ |
| `usuarios:visualizar:usuario` | Visualizar lista e detalhes de usuários | ❌ | ❌ | ✅ | ✅ |
| `usuarios:inativar:usuario` | Inativar usuários do sistema | ❌ | ❌ | ❌ | ✅ |
| `usuarios:reativar:usuario` | Reativar usuários que estavam inativos | ❌ | ❌ | ❌ | ✅ |
| `usuarios:gerenciar:roles` | Gerenciar roles atribuídas aos usuários | ❌ | ❌ | ❌ | ✅ |

### ⚙️ MÓDULO: Configurações
| Permissão | Descrição | Operador | Supervisor | Gestor | Admin |
|-----------|-----------|----------|------------|--------|-------|
| `configuracoes:criar:role` | Criar novas roles no sistema | ❌ | ❌ | ❌ | ✅ |
| `configuracoes:editar:role` | Editar roles existentes (apenas customizadas) | ❌ | ❌ | ❌ | ✅ |
| `configuracoes:visualizar:role` | Visualizar roles e suas permissões | ❌ | ❌ | ❌ | ✅ |
| `configuracoes:deletar:role` | Deletar roles customizadas (não padrão) | ❌ | ❌ | ❌ | ✅ |

### 📋 MÓDULO: Auditorias
| Permissão | Descrição | Operador | Supervisor | Gestor | Admin |
|-----------|-----------|----------|------------|--------|-------|
| `auditorias:criar:auditoria` | Criar novas auditorias no sistema | ✅ | ✅ | ✅ | ✅ |
| `auditorias:editar:auditoria` | Editar auditorias em andamento | ✅ | ✅ | ✅ | ✅ |
| `auditorias:visualizar:auditoria` | Visualizar auditorias e seus resultados | ✅ | ✅ | ✅ | ✅ |
| `auditorias:finalizar:auditoria` | Finalizar auditorias marcando como concluídas | ❌ | ✅ | ✅ | ✅ |
| `auditorias:arquivar:auditoria` | Arquivar auditorias antigas | ❌ | ❌ | ✅ | ✅ |
| `auditorias:exportar:relatorio` | Exportar relatórios de auditoria em PDF/Excel | ✅ | ✅ | ✅ | ✅ |
| `auditorias:criar:modelo` | Criar novos modelos de checklist | ❌ | ❌ | ✅ | ✅ |
| `auditorias:editar:modelo` | Editar modelos de checklist existentes | ❌ | ❌ | ✅ | ✅ |
| `auditorias:visualizar:modelo` | Visualizar modelos de checklist disponíveis | ✅ | ✅ | ✅ | ✅ |
| `auditorias:deletar:modelo` | Deletar modelos de checklist | ❌ | ❌ | ✅ | ✅ |

### 🦺 MÓDULO: EPIs (Equipamentos de Proteção Individual)
| Permissão | Descrição | Operador | Supervisor | Gestor | Admin |
|-----------|-----------|----------|------------|--------|-------|
| `epis:visualizar:estoque` | Visualizar estoque local de EPIs | ❌ | ✅ | ✅ | ✅ |
| `epis:visualizar:geral_estoque` | Visualizar todos os estoques de EPIs da empresa | ❌ | ❌ | ✅ | ✅ |
| `epis:gerenciar:estoque` | Gerenciar entrada/saída e movimentação de estoque | ❌ | ❌ | ❌ | ✅ |
| `epis:solicitar:epi` | Solicitar EPIs para funcionários | ✅ | ✅ | ✅ | ✅ |
| `epis:aprovar:solicitacao` | Aprovar solicitações de EPI de funcionários | ❌ | ✅ | ✅ | ✅ |
| `epis:rejeitar:solicitacao` | Rejeitar solicitações de EPI inadequadas | ❌ | ✅ | ✅ | ✅ |
| `epis:entregar:epi` | Registrar entrega física de EPIs aos funcionários | ❌ | ✅ | ✅ | ✅ |
| `epis:devolver:epi` | Processar devolução de EPIs usados | ❌ | ✅ | ✅ | ✅ |
| `epis:criar:item_epi` | Cadastrar novos tipos de EPI no sistema | ❌ | ❌ | ✅ | ✅ |
| `epis:editar:item_epi` | Editar informações de EPIs existentes | ❌ | ❌ | ✅ | ✅ |
| `epis:inativar:item_epi` | Inativar EPIs que não são mais utilizados | ❌ | ❌ | ✅ | ✅ |

#### Riscos Ocupacionais
| Permissão | Descrição | Operador | Supervisor | Gestor | Admin |
|-----------|-----------|----------|------------|--------|-------|
| `epis:criar:risco_ocupacional` | Cadastrar novos riscos ocupacionais | ❌ | ❌ | ✅ | ✅ |
| `epis:visualizar:todos_risco_ocupacional` | Visualizar todos os riscos cadastrados | ❌ | ❌ | ✅ | ✅ |
| `epis:editar:risco_ocupacional` | Editar riscos ocupacionais existentes | ❌ | ❌ | ✅ | ✅ |
| `epis:inativar:risco_ocupacional` | Inativar riscos que não são mais relevantes | ❌ | ❌ | ✅ | ✅ |

#### Configurações de EPIs NR-6
| Permissão | Descrição | Operador | Supervisor | Gestor | Admin |
|-----------|-----------|----------|------------|--------|-------|
| `epis:visualizar:todos_epi_configuracao` | Ver todos os EPIs NR-6 customizados | ❌ | ❌ | ✅ | ✅ |
| `epis:criar:epi_configuracao` | Cadastrar EPIs NR-6 personalizados | ❌ | ❌ | ✅ | ✅ |
| `epis:inativar:epi_configuracao` | Inativar configurações de EPIs NR-6 | ❌ | ❌ | ✅ | ✅ |

#### Motivos de Solicitação
| Permissão | Descrição | Operador | Supervisor | Gestor | Admin |
|-----------|-----------|----------|------------|--------|-------|
| `epis:visualizar:todos_motivos` | Visualizar todos os motivos de solicitação | ✅ | ✅ | ✅ | ✅ |
| `epis:criar:motivo` | Criar novos motivos de solicitação de EPI | ❌ | ❌ | ✅ | ✅ |
| `epis:inativar:motivo` | Inativar motivos não utilizados | ❌ | ❌ | ✅ | ✅ |

#### GHE (Grupos Homogêneos de Exposição)
| Permissão | Descrição | Operador | Supervisor | Gestor | Admin |
|-----------|-----------|----------|------------|--------|-------|
| `epis:criar:ghe` | Cadastrar novos Grupos Homogêneos de Exposição | ❌ | ❌ | ✅ | ✅ |
| `epis:editar:ghe` | Editar GHEs existentes | ❌ | ❌ | ✅ | ✅ |
| `epis:visualizar:ghe` | Visualizar GHEs do seu contexto | ❌ | ✅ | ✅ | ✅ |
| `epis:visualizar:todos_ghe` | Visualizar todos os GHEs da empresa | ❌ | ❌ | ✅ | ✅ |
| `epis:inativar:ghe` | Inativar GHEs não utilizados | ❌ | ❌ | ✅ | ✅ |
| `epis:associar:ghe_epi` | Associar EPIs aos GHEs | ❌ | ❌ | ✅ | ✅ |

#### Fabricantes
| Permissão | Descrição | Operador | Supervisor | Gestor | Admin |
|-----------|-----------|----------|------------|--------|-------|
| `epis:criar:fabricante` | Cadastrar novos fabricantes de EPI | ❌ | ❌ | ✅ | ✅ |
| `epis:editar:fabricante` | Editar dados de fabricantes | ❌ | ❌ | ✅ | ✅ |
| `epis:visualizar:fabricante` | Visualizar lista básica de fabricantes | ✅ | ✅ | ✅ | ✅ |
| `epis:visualizar:todos_fabricante` | Visualizar todos os fabricantes e detalhes | ❌ | ❌ | ✅ | ✅ |
| `epis:inativar:fabricante` | Inativar fabricantes não utilizados | ❌ | ❌ | ✅ | ✅ |

### 📊 MÓDULO: Relatórios
| Permissão | Descrição | Operador | Supervisor | Gestor | Admin |
|-----------|-----------|----------|------------|--------|-------|
| `relatorios:visualizar:epi-dashboard` | Acessar dashboard principal de EPIs | ❌ | ✅ | ✅ | ✅ |
| `relatorios:visualizar:auditoria-dashboard` | Acessar dashboard principal de auditorias | ❌ | ✅ | ✅ | ✅ |
| `relatorios:visualizar:formulario-dashboard` | Acessar dashboard principal de formulários | ❌ | ✅ | ✅ | ✅ |
| `relatorios:gerar:formulario-pdf` | Gerar relatórios de formulários em PDF | ❌ | ❌ | ✅ | ✅ |
| `relatorios:gerar:formulario-excel` | Gerar relatórios de formulários em Excel | ❌ | ❌ | ✅ | ✅ |
| `relatorios:gerar:epi_inventario` | Gerar relatórios de inventário de EPIs | ❌ | ❌ | ✅ | ✅ |
| `relatorios:gerar:epi_devolucao` | Gerar relatórios de devolução de EPIs | ❌ | ❌ | ✅ | ✅ |
| `relatorios:gerar:epi_assinatura` | Gerar relatórios de assinatura de EPIs | ❌ | ❌ | ✅ | ✅ |

### 🏗️ MÓDULO: Estrutura Organizacional
| Permissão | Descrição | Operador | Supervisor | Gestor | Admin |
|-----------|-----------|----------|------------|--------|-------|
| `estrutura:criar:local_trabalho` | Criar novos locais de trabalho | ❌ | ❌ | ✅ | ✅ |
| `estrutura:editar:local_trabalho` | Editar informações de locais de trabalho | ❌ | ❌ | ✅ | ✅ |
| `estrutura:visualizar:local_trabalho` | Visualizar locais de trabalho do contexto | ✅ | ✅ | ✅ | ✅ |
| `estrutura:visualizar:todos_local_trabalho` | Visualizar todos os locais da empresa | ❌ | ❌ | ✅ | ✅ |
| `estrutura:inativar:local_trabalho` | Inativar locais de trabalho | ❌ | ❌ | ✅ | ✅ |

#### Setores
| Permissão | Descrição | Operador | Supervisor | Gestor | Admin |
|-----------|-----------|----------|------------|--------|-------|
| `estrutura:criar:setor` | Criar novos setores | ❌ | ❌ | ✅ | ✅ |
| `estrutura:editar:setor` | Editar informações de setores | ❌ | ❌ | ✅ | ✅ |
| `estrutura:visualizar:setor` | Visualizar setores do contexto | ✅ | ✅ | ✅ | ✅ |
| `estrutura:visualizar:todos_setor` | Visualizar todos os setores da empresa | ❌ | ❌ | ✅ | ✅ |
| `estrutura:inativar:setor` | Inativar setores não utilizados | ❌ | ❌ | ✅ | ✅ |

#### Cargos
| Permissão | Descrição | Operador | Supervisor | Gestor | Admin |
|-----------|-----------|----------|------------|--------|-------|
| `estrutura:criar:cargo` | Criar novos cargos | ❌ | ❌ | ✅ | ✅ |
| `estrutura:editar:cargo` | Editar informações de cargos | ❌ | ❌ | ✅ | ✅ |
| `estrutura:visualizar:cargo` | Visualizar cargos do contexto | ✅ | ✅ | ✅ | ✅ |
| `estrutura:visualizar:todos_cargo` | Visualizar todos os cargos da empresa | ❌ | ❌ | ✅ | ✅ |
| `estrutura:inativar:cargo` | Inativar cargos não utilizados | ❌ | ❌ | ✅ | ✅ |

#### Empresas Terceiras
| Permissão | Descrição | Operador | Supervisor | Gestor | Admin |
|-----------|-----------|----------|------------|--------|-------|
| `estrutura:criar:terceiro` | Cadastrar empresas terceiras | ❌ | ❌ | ✅ | ✅ |
| `estrutura:editar:terceiro` | Editar dados de empresas terceiras | ❌ | ❌ | ✅ | ✅ |
| `estrutura:visualizar:todos_terceiro` | Visualizar todas as empresas terceiras | ❌ | ❌ | ✅ | ✅ |
| `estrutura:inativar:terceiro` | Inativar empresas terceiras | ❌ | ❌ | ✅ | ✅ |

### 👷 MÓDULO: Funcionários
| Permissão | Descrição | Operador | Supervisor | Gestor | Admin |
|-----------|-----------|----------|------------|--------|-------|
| `funcionarios:criar:funcionario` | Cadastrar novos funcionários | ❌ | ❌ | ✅ | ✅ |
| `funcionarios:editar:funcionario` | Editar dados de funcionários | ❌ | ✅ | ✅ | ✅ |
| `funcionarios:visualizar:funcionario` | Visualizar lista de funcionários | ✅ | ✅ | ✅ | ✅ |
| `funcionarios:inativar:funcionario` | Inativar funcionários que saíram | ❌ | ❌ | ✅ | ✅ |
| `funcionarios:reativar:funcionario` | Reativar funcionários que retornaram | ❌ | ❌ | ✅ | ✅ |
| `funcionarios:gerenciar:reconhecimento_facial` | Gerenciar cadastro de reconhecimento facial | ❌ | ✅ | ✅ | ✅ |

### 📝 MÓDULO: Formulários
| Permissão | Descrição | Operador | Supervisor | Gestor | Admin |
|-----------|-----------|----------|------------|--------|-------|
| `formularios:criar:modelo_formulario` | Criar novos modelos de formulário | ❌ | ❌ | ✅ | ✅ |
| `formularios:editar:modelo_formulario` | Editar modelos de formulário existentes | ❌ | ❌ | ✅ | ✅ |
| `formularios:visualizar:modelo_formulario` | Visualizar modelos de formulário disponíveis | ✅ | ✅ | ✅ | ✅ |
| `formularios:deletar:modelo_formulario` | Deletar modelos de formulário | ❌ | ❌ | ✅ | ✅ |
| `formularios:criar:formulario` | Criar instâncias de formulários | ✅ | ✅ | ✅ | ✅ |
| `formularios:visualizar:formulario` | Visualizar formulários do contexto | ✅ | ✅ | ✅ | ✅ |
| `formularios:editar:formulario` | Editar configurações de formulários | ✅ | ✅ | ✅ | ✅ |
| `formularios:preencher:registro` | Preencher registros nos formulários | ✅ | ✅ | ✅ | ✅ |

### 🏢 MÓDULO: Empresa
| Permissão | Descrição | Operador | Supervisor | Gestor | Admin |
|-----------|-----------|----------|------------|--------|-------|
| `empresa:editar:configuracoes` | Editar configurações gerais da empresa | ❌ | ❌ | ❌ | ✅ |
| `empresa:visualizar:configuracoes` | Visualizar configurações da empresa | ❌ | ❌ | ✅ | ✅ |
| `empresa:configurar:whatsapp` | Configurar integração com WhatsApp | ❌ | ❌ | ❌ | ✅ |

## Como Atribuir Roles aos Usuários

{% hint style="info" %}
**Pré-requisito**: Você precisa ter a permissão `usuarios:gerenciar:roles` para atribuir roles a outros usuários. Por padrão, apenas usuários com role "Administrador" possuem esta permissão.
{% endhint %}

### Atribuição Básica
1. Acesse **Configurações** → **Usuários**
2. Selecione o usuário desejado
3. Na seção **"Roles e Permissões"**, clique em **"Gerenciar Roles"**
4. Selecione uma ou mais roles para o usuário
5. Salve as alterações

### Atribuição Contextual
Para maior flexibilidade, você pode atribuir roles específicas para determinados contextos:

**Por Unidade de Trabalho:**
- Um usuário pode ser **Supervisor** na Unidade A
- E **Operador** na Unidade B

**Por Setor:**
- Um usuário pode ser **Gestor** no Setor de Manutenção
- E **Supervisor** no Setor de Produção

**Exemplo Prático:**
```
João Silva:
├── Role: Gestor (Unidade: Fábrica SP, Setor: Manutenção)
├── Role: Supervisor (Unidade: Fábrica SP, Setor: Produção)
└── Role: Operador (Unidade: Fábrica RJ, Todos os setores)
```

{% hint style="warning" %}
**Cuidado com Conflitos**: Quando um usuário tem múltiplas roles, o sistema sempre aplica a permissão mais ampla. Se há conflito, a role com maior privilégio prevalece.
{% endhint %}

## Criando Roles Personalizadas

{% hint style="info" %}
**Flexibilidade Total**: O sistema permite criar quantas roles personalizadas forem necessárias. Você pode combinar permissões de diferentes módulos para atender necessidades específicas da sua organização.
{% endhint %}

Para necessidades específicas da sua organização, você pode criar roles customizadas:

### Passos para Criar uma Nova Role

1. Acesse **Configurações** → **Roles e Permissões**
2. Clique em **"Nova Role"**
3. Preencha as informações:
   - **Nome**: Nome descritivo da role
   - **Descrição**: Explicação do propósito da role
   - **Tipo**: Customizada (não é uma role do sistema)

### Definindo Permissões

4. Na seção **"Permissões"**, selecione as ações permitidas por módulo
5. Use os templates das roles padrão como base:
   - **Começar com Operador**: Para roles mais restritivas
   - **Começar com Supervisor**: Para roles intermediárias
   - **Começar com Gestor**: Para roles mais amplas

{% hint style="warning" %}
**Roles do Sistema**: As 4 roles padrão (Operador, Supervisor, Gestor, Administrador) não podem ser editadas ou deletadas, pois são fundamentais para o funcionamento do sistema.
{% endhint %}

### Exemplos de Roles Customizadas

**Técnico de Segurança:**
- Todas as permissões de auditorias
- Visualizar todos os EPIs e estoque
- Criar relatórios de segurança
- Sem acesso a usuários ou configurações

**Almoxarife:**
- Gerenciar completamente estoque de EPIs
- Processar solicitações e devoluções
- Gerar relatórios de inventário
- Visualizar funcionários (para entregas)
- Sem acesso a auditorias

**Analista de Dados:**
- Visualizar todas as auditorias
- Gerar todos os tipos de relatórios
- Visualizar formulários e registros
- Sem poder criar ou editar dados

{% hint style="info" %}
**Dica**: Ao criar roles personalizadas, sempre teste com um usuário de teste antes de aplicar em produção. Isso evita problemas de acesso não intencionais.
{% endhint %}

## Boas Práticas de Segurança

### Princípio do Menor Privilégio
- Conceda apenas as permissões mínimas necessárias
- Revise regularmente as permissões atribuídas
- Remova acessos de usuários que mudaram de função

### Segregação de Funções
- Separe responsabilidades críticas entre diferentes usuários
- Evite concentrar muitas permissões em uma única pessoa
- Use aprovações de diferentes níveis para ações importantes

### Auditoria de Acessos
- Monitore regularmente quem tem acesso a quê
- Mantenha um log das alterações de permissões
- Revise periodicamente roles e usuários inativos

### Gestão de Roles
- Mantenha as roles organizadas e bem documentadas
- Use nomes descritivos para roles customizadas
- Evite duplicação desnecessária de roles

{% hint style="warning" %}
**Auditoria Regular**: Revise periodicamente as roles customizadas e remova aquelas que não estão mais em uso. Isso mantém o sistema organizado e reduz riscos de segurança.
{% endhint %}

## Casos de Uso Comuns

### Scenario 1: Empresa Multi-Unidades
**Situação**: Empresa com 5 fábricas, cada uma com gestão local

**Solução**:
- Administrador geral com acesso a todas as unidades
- Gestor local para cada fábrica (acesso apenas à sua unidade)
- Supervisores por setor dentro de cada fábrica
- Operadores com acesso apenas ao seu setor

{% hint style="info" %}
**Escalabilidade**: Este modelo escala perfeitamente quando a empresa cresce. Novas unidades podem ser adicionadas sem impactar a estrutura de permissões existente.
{% endhint %}

### Scenario 2: Empresa com Terceiros
**Situação**: Funcionários próprios + empresas terceirizadas

**Solução**:
- Role "Terceirizado" com permissões limitadas
- Acesso apenas a auditorias específicas
- Sem visualização de dados financeiros ou estoque
- Relatórios restritos apenas às suas atividades

### Scenario 3: Consultoria Especializada
**Situação**: Consultores externos fazendo auditorias

**Solução**:
- Role "Consultor" temporária
- Acesso apenas ao módulo de auditorias
- Sem visualização de funcionários ou estrutura interna
- Exportação limitada de relatórios

{% hint style="warning" %}
**Tempo Limitado**: Para consultores externos, considere sempre definir uma data de expiração para as roles atribuídas, removendo o acesso automaticamente após o término do projeto.
{% endhint %}

## Troubleshooting

{% hint style="info" %}
**Cache de Permissões**: O sistema mantém um cache das permissões do usuário. Se as alterações não surtirem efeito imediatamente, peça para o usuário fazer logout e login novamente.
{% endhint %}

### Usuário não consegue acessar uma funcionalidade
1. Verifique se o usuário tem a role adequada
2. Confirme se a role tem a permissão específica
3. Verifique se o contexto (unidade/setor) está correto
4. Confirme se o usuário está ativo

### Role personalizada não aparece
1. Verifique se a role foi salva corretamente
2. Confirme se a role não está inativa
3. Verifique se você tem permissão para gerenciar roles

### Permissões não funcionam como esperado
1. Logue out e logue in novamente
2. Verifique conflitos entre multiple roles
3. Confirme a hierarquia de permissões
4. Contate o suporte se necessário

{% hint style="warning" %}
**Suporte Técnico**: Se você encontrar problemas persistentes com permissões, documente exatamente quais ações o usuário estava tentando realizar e quais mensagens de erro apareceram antes de entrar em contato com o suporte.
{% endhint %}

## Migração de Usuários Existentes

Durante a implementação do novo sistema de roles, todos os usuários existentes foram automaticamente migrados:

- **Operador** → Role "Operador"
- **Supervisor** → Role "Supervisor" 
- **Gestor** → Role "Gestor"
- **Admin** → Role "Administrador"
- **Usuários sem tipo** → Role "Operador" (padrão seguro)

As permissões foram mantidas compatíveis com o sistema anterior, garantindo que nenhum usuário perca acesso às funcionalidades que já utilizava.

{% hint style="info" %}
**Transição Suave**: A migração foi projetada para ser transparente. Usuários não notarão diferenças no acesso, mas administradores agora têm muito mais flexibilidade para personalizar permissões.
{% endhint %}

---

{% hint style="warning" %}
**Documentação Viva**: Este sistema está em constante evolução. Novas permissões podem ser adicionadas conforme novos módulos são desenvolvidos. Mantenha-se atualizado com as mudanças do sistema.
{% endhint %}

*Esta documentação cobre os aspectos principais do sistema de roles e permissões. Para dúvidas específicas ou cenários não cobertos, entre em contato com o suporte técnico.*