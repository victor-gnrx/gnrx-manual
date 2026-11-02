---
description: Lista completa das permissões de cada role, módulo por módulo.
icon: shield-check
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
    visible: false
  tags:
    visible: true
  actions:
    visible: true
---

# Consultar as permissões

**Para que serve:** ver, módulo por módulo, o que cada role padrão pode fazer.

{% hint style="info" %}
**Quem pode fazer:** qualquer pessoa pode ler esta página. Para criar ou mudar roles no sistema, você precisa ser Administrador.
{% endhint %}

## Antes de começar

* Leia primeiro [Entender as roles](o-que-sao-roles.md). Lá está o resumo de cada role.
* ✓ quer dizer que a role tem a permissão. O **Acesso Empresa (CNPJ)** tem todas.
* A coluna **Chave** é o nome técnico da permissão.

## Permissões por módulo

<details>

<summary>Auditorias (11)</summary>

| Permissão | Chave | Operador | Supervisor | Gestor | Administrador |
| --- | --- | :-: | :-: | :-: | :-: |
| Arquivar auditorias | `auditorias:arquivar:auditoria` |  |  | ✓ | ✓ |
| Criar modelos de checklist | `auditorias:criar:modelo` |  |  | ✓ | ✓ |
| Criar novas auditorias | `auditorias:criar:auditoria` | ✓ | ✓ | ✓ | ✓ |
| Deletar modelos de checklist | `auditorias:deletar:modelo` |  |  | ✓ | ✓ |
| Editar auditorias em andamento | `auditorias:editar:auditoria` | ✓ | ✓ | ✓ | ✓ |
| Editar modelos de checklist | `auditorias:editar:modelo` |  |  | ✓ | ✓ |
| Exportar relatórios de auditoria | `auditorias:exportar:relatorio` | ✓ | ✓ | ✓ | ✓ |
| Finalizar auditorias em andamento | `auditorias:finalizar:auditoria` | ✓ | ✓ | ✓ | ✓ |
| Visualizar auditorias de todos os usuários | `auditorias:visualizar:todos_auditoria` |  |  | ✓ | ✓ |
| Visualizar auditorias e resultados | `auditorias:visualizar:auditoria` | ✓ | ✓ | ✓ | ✓ |
| Visualizar modelos de checklist | `auditorias:visualizar:modelo` | ✓ | ✓ | ✓ | ✓ |

</details>

<details>

<summary>Colaboradores (10)</summary>

| Permissão | Chave | Operador | Supervisor | Gestor | Administrador |
| --- | --- | :-: | :-: | :-: | :-: |
| Anexar fichas de EPI retroativas ao perfil do colaborador | `funcionarios:criar:ficha_retroativa` |  |  | ✓ | ✓ |
| Cadastrar novos funcionários | `funcionarios:criar:funcionario` |  |  |  | ✓ |
| Editar dados de funcionários | `funcionarios:editar:funcionario` |  | ✓ | ✓ | ✓ |
| Enviar o termo de responsabilidade para assinatura por e-mail | `funcionarios:notificar:assinatura_termo` |  |  | ✓ | ✓ |
| Excluir fichas de EPI retroativas do colaborador | `funcionarios:excluir:ficha_retroativa` |  |  | ✓ | ✓ |
| Gerenciar reconhecimento facial | `funcionarios:gerenciar:reconhecimento_facial` |  |  | ✓ | ✓ |
| Inativar funcionários | `funcionarios:inativar:funcionario` |  |  |  | ✓ |
| Reativar funcionários | `funcionarios:reativar:funcionario` |  |  | ✓ | ✓ |
| Visualizar fichas de EPI retroativas do colaborador | `funcionarios:visualizar:ficha_retroativa` | ✓ | ✓ | ✓ | ✓ |
| Visualizar lista de funcionários | `funcionarios:visualizar:funcionario` | ✓ | ✓ | ✓ | ✓ |

</details>

<details>

<summary>Configurações (roles) (4)</summary>

| Permissão | Chave | Operador | Supervisor | Gestor | Administrador |
| --- | --- | :-: | :-: | :-: | :-: |
| Criar novas roles | `configuracoes:criar:role` |  |  |  | ✓ |
| Deletar roles customizadas | `configuracoes:deletar:role` |  |  |  | ✓ |
| Editar roles existentes | `configuracoes:editar:role` |  |  |  | ✓ |
| Visualizar roles e permissões | `configuracoes:visualizar:role` |  |  |  | ✓ |

</details>

<details>

<summary>DDS (5)</summary>

| Permissão | Chave | Operador | Supervisor | Gestor | Administrador |
| --- | --- | :-: | :-: | :-: | :-: |
| Cadastrar e editar os temas de DDS da empresa | `dds:gerenciar:tema` |  |  | ✓ | ✓ |
| Programar as agendas recorrentes de DDS | `dds:gerenciar:agenda` |  |  | ✓ | ✓ |
| Registrar, conduzir, concluir e cancelar DDS | `dds:gerenciar:dds` |  | ✓ | ✓ | ✓ |
| Visualizar o painel de adesão aos DDS | `dds:visualizar:painel` |  | ✓ | ✓ | ✓ |
| Visualizar os DDS (Diálogos Diários de Segurança) | `dds:visualizar:dds` | ✓ | ✓ | ✓ | ✓ |

</details>

<details>

<summary>Empresa (4)</summary>

| Permissão | Chave | Operador | Supervisor | Gestor | Administrador |
| --- | --- | :-: | :-: | :-: | :-: |
| Configurar a exigência do termo de responsabilidade na entrada do app | `empresa:alterar:politica_termo_app` |  |  | ✓ | ✓ |
| Configurar integração WhatsApp | `empresa:configurar:whatsapp` |  |  |  | ✓ |
| Editar configurações da empresa | `empresa:editar:configuracoes` |  |  |  | ✓ |
| Visualizar configurações da empresa | `empresa:visualizar:configuracoes` |  |  | ✓ | ✓ |

</details>

<details>

<summary>Estruturas (32)</summary>

| Permissão | Chave | Operador | Supervisor | Gestor | Administrador |
| --- | --- | :-: | :-: | :-: | :-: |
| Cadastrar turnos | `estrutura:criar:turno` |  |  |  | ✓ |
| Criar cargos | `estrutura:criar:cargo` |  |  |  | ✓ |
| Criar centros de custo | `estrutura:criar:centro_custo` |  |  | ✓ | ✓ |
| Criar centros de estoque | `estrutura:criar:centro_estoque` |  |  | ✓ | ✓ |
| Criar locais de trabalho | `estrutura:criar:local_trabalho` |  |  |  | ✓ |
| Criar setores | `estrutura:criar:setor` |  |  |  | ✓ |
| Criar terceiros | `estrutura:criar:terceiro` |  |  |  | ✓ |
| Editar cargos | `estrutura:editar:cargo` |  |  | ✓ | ✓ |
| Editar centros de custo | `estrutura:editar:centro_custo` |  |  | ✓ | ✓ |
| Editar centros de estoque | `estrutura:editar:centro_estoque` |  |  | ✓ | ✓ |
| Editar locais de trabalho | `estrutura:editar:local_trabalho` |  |  | ✓ | ✓ |
| Editar setores | `estrutura:editar:setor` |  |  | ✓ | ✓ |
| Editar terceiros | `estrutura:editar:terceiro` |  |  | ✓ | ✓ |
| Editar turnos, horários e unir turnos | `estrutura:editar:turno` |  |  | ✓ | ✓ |
| Inativar cargos | `estrutura:inativar:cargo` |  |  |  | ✓ |
| Inativar centros de custo | `estrutura:inativar:centro_custo` |  |  | ✓ | ✓ |
| Inativar centros de estoque | `estrutura:inativar:centro_estoque` |  |  | ✓ | ✓ |
| Inativar locais de trabalho | `estrutura:inativar:local_trabalho` |  |  |  | ✓ |
| Inativar setores | `estrutura:inativar:setor` |  |  |  | ✓ |
| Inativar terceiros | `estrutura:inativar:terceiro` |  |  |  | ✓ |
| Inativar turnos | `estrutura:inativar:turno` |  |  |  | ✓ |
| Visualizar cargos | `estrutura:visualizar:cargo` |  |  | ✓ | ✓ |
| Visualizar centro de custo | `estrutura:visualizar:centro_custo` | ✓ | ✓ | ✓ | ✓ |
| Visualizar centro de estoque | `estrutura:visualizar:centro_estoque` | ✓ | ✓ | ✓ | ✓ |
| Visualizar locais de trabalho | `estrutura:visualizar:local_trabalho` | ✓ | ✓ | ✓ | ✓ |
| Visualizar os turnos da empresa | `estrutura:visualizar:turno` |  |  | ✓ | ✓ |
| Visualizar setor | `estrutura:visualizar:setor` | ✓ | ✓ | ✓ | ✓ |
| Visualizar todos os cargos | `estrutura:visualizar:todos_cargo` |  |  | ✓ | ✓ |
| Visualizar todos os centros de custo | `estrutura:visualizar:todos_centro_custo` | ✓ | ✓ | ✓ | ✓ |
| Visualizar todos os locais de trabalho | `estrutura:visualizar:todos_local_trabalho` |  |  | ✓ | ✓ |
| Visualizar todos os setores | `estrutura:visualizar:todos_setor` |  |  | ✓ | ✓ |
| Visualizar todos os terceiros | `estrutura:visualizar:todos_terceiro` |  |  | ✓ | ✓ |

</details>

<details>

<summary>Fluxos de aprovação (4)</summary>

| Permissão | Chave | Operador | Supervisor | Gestor | Administrador |
| --- | --- | :-: | :-: | :-: | :-: |
| Criar, editar, publicar, pausar e excluir fluxos de aprovação | `fluxos:gerenciar:fluxo_aprovacao` |  |  | ✓ | ✓ |
| Decidir as etapas de aprovação atribuídas a si | `fluxos:aprovar:solicitacao` |  | ✓ | ✓ | ✓ |
| Reatribuir etapas de fluxos que travaram sem aprovador | `fluxos:destravar:instancia` |  |  | ✓ | ✓ |
| Visualizar fluxos de aprovação e o andamento das solicitações neles | `fluxos:visualizar:fluxo_aprovacao` |  | ✓ | ✓ | ✓ |

</details>

<details>

<summary>Formulários (8)</summary>

| Permissão | Chave | Operador | Supervisor | Gestor | Administrador |
| --- | --- | :-: | :-: | :-: | :-: |
| Criar formulários | `formularios:criar:formulario` | ✓ | ✓ | ✓ | ✓ |
| Criar modelos de formulário | `formularios:criar:modelo_formulario` |  |  | ✓ | ✓ |
| Deletar modelos de formulário | `formularios:deletar:modelo_formulario` |  |  | ✓ | ✓ |
| Editar formulários | `formularios:editar:formulario` | ✓ | ✓ | ✓ | ✓ |
| Editar modelos de formulário | `formularios:editar:modelo_formulario` |  |  | ✓ | ✓ |
| Preencher registros de formulário | `formularios:preencher:registro` | ✓ | ✓ | ✓ | ✓ |
| Visualizar formulário | `formularios:visualizar:formulario` | ✓ | ✓ | ✓ | ✓ |
| Visualizar modelos de formulário | `formularios:visualizar:modelo_formulario` | ✓ | ✓ | ✓ | ✓ |

</details>

<details>

<summary>Fornecedores (5)</summary>

| Permissão | Chave | Operador | Supervisor | Gestor | Administrador |
| --- | --- | :-: | :-: | :-: | :-: |
| Criar fornecedor | `fornecedores:criar:fornecedor` |  | ✓ | ✓ | ✓ |
| Editar fornecedor | `fornecedores:editar:fornecedor` |  | ✓ | ✓ | ✓ |
| Inativar fornecedor | `fornecedores:inativar:fornecedor` |  | ✓ | ✓ | ✓ |
| Vincular e precificar itens do fornecedor | `fornecedores:vincular:item` |  | ✓ | ✓ | ✓ |
| Visualizar fornecedores, comparativos e relatórios | `fornecedores:visualizar:fornecedor` |  | ✓ | ✓ | ✓ |

</details>

<details>

<summary>Gestão de Acidentes (11)</summary>

| Permissão | Chave | Operador | Supervisor | Gestor | Administrador |
| --- | --- | :-: | :-: | :-: | :-: |
| Assinar e transmitir a CAT ao eSocial | `acidentes:transmitir:cat` |  |  | ✓ | ✓ |
| Conduzir a investigação da ocorrência | `acidentes:investigar:ocorrencia` |  | ✓ | ✓ | ✓ |
| Criar plano de ação a partir da ocorrência | `acidentes:criar:plano_acao` |  | ✓ | ✓ | ✓ |
| Editar as configurações do módulo e as horas-homem | `acidentes:editar:configuracao` |  |  | ✓ | ✓ |
| Lançar custos dos acidentes | `acidentes:gerenciar:custo` |  |  | ✓ | ✓ |
| Preencher a CAT (S-2210) e informar o recibo | `acidentes:gerenciar:cat` |  |  | ✓ | ✓ |
| Registrar ocorrências (desvio, quase-acidente, acidente) | `acidentes:registrar:ocorrencia` | ✓ | ✓ | ✓ | ✓ |
| Triar e tratar ocorrências: classificar, responsável, envolvidos, testemunhas, anexos, status | `acidentes:gerenciar:ocorrencia` |  | ✓ | ✓ | ✓ |
| Ver dados de saúde do acidentado (CAT, CID, atestado, fotos de lesão) | `acidentes:visualizar:dados_saude` |  |  | ✓ | ✓ |
| Ver os custos dos acidentes | `acidentes:visualizar:custo` |  |  | ✓ | ✓ |
| Visualizar ocorrências e acidentes | `acidentes:visualizar:ocorrencia` | ✓ | ✓ | ✓ | ✓ |

</details>

<details>

<summary>Gestão de CIPA (18)</summary>

| Permissão | Chave | Operador | Supervisor | Gestor | Administrador |
| --- | --- | :-: | :-: | :-: | :-: |
| Abrir levantamentos de percepção de riscos e registrar o mapa de risco (NR-5 5.3.1 b) | `cipa:gerenciar:percepcao_risco` |  | ✓ | ✓ | ✓ |
| Apurar a eleição da CIPA e dar posse | `cipa:apurar:eleicao` |  |  | ✓ | ✓ |
| Cancelar um processo eleitoral da CIPA | `cipa:cancelar:eleicao` |  |  | ✓ | ✓ |
| Conduzir o processo eleitoral (edital, sindicato, inscrições, votação) | `cipa:conduzir:eleicao` |  | ✓ | ✓ | ✓ |
| Criar plano de ação a partir da CIPA | `cipa:criar:plano_acao` |  | ✓ | ✓ | ✓ |
| Editar as configurações da CIPA da empresa | `cipa:editar:configuracao` |  |  | ✓ | ✓ |
| Editar os dados da CIPA da unidade (CNAE, grau de risco) e os feriados | `cipa:editar:unidade` |  |  | ✓ | ✓ |
| Gerenciar membros, cargos, calendário e treinamento da CIPA | `cipa:gerenciar:mandato` |  |  | ✓ | ✓ |
| Gerenciar os representantes das contratadas na CIPA (NR-5 5.8) | `cipa:gerenciar:contratada` |  |  | ✓ | ✓ |
| Gerenciar reuniões, presença e atas da CIPA | `cipa:gerenciar:reuniao` |  | ✓ | ✓ | ✓ |
| Nomear o representante da NR-5 | `cipa:gerenciar:nomeacao` |  |  | ✓ | ✓ |
| Planejar a SIPAT, as atividades e a presença (NR-5 5.3.1 i) | `cipa:gerenciar:sipat` |  | ✓ | ✓ | ✓ |
| Publicar as regras de conduta sobre assédio (Lei 14.457/2022) | `cipa:editar:codigo_conduta` |  |  | ✓ | ✓ |
| Receber e apurar as denúncias de assédio e violência (acesso restrito) | `cipa:gerenciar:denuncia` |  |  |  | ✓ |
| Visualizar a estabilidade de candidatos e eleitos da CIPA | `cipa:visualizar:estabilidade` |  | ✓ | ✓ | ✓ |
| Visualizar as unidades e o dimensionamento da CIPA | `cipa:visualizar:unidade` | ✓ | ✓ | ✓ | ✓ |
| Visualizar mandatos, membros e reuniões da CIPA | `cipa:visualizar:mandato` | ✓ | ✓ | ✓ | ✓ |
| Visualizar processos eleitorais da CIPA | `cipa:visualizar:eleicao` | ✓ | ✓ | ✓ | ✓ |

</details>

<details>

<summary>Gestão de Documentos (16)</summary>

| Permissão | Chave | Operador | Supervisor | Gestor | Administrador |
| --- | --- | :-: | :-: | :-: | :-: |
| Abrir documentos de saúde (ASO, atestado) — dado sensível | `documentos:visualizar:documento_sensivel` |  |  | ✓ | ✓ |
| Aprovar e reprovar documentos enviados | `documentos:analisar:documento` |  |  | ✓ | ✓ |
| Aprovar ou reprovar liberação excepcional | `documentos:aprovar:liberacao` |  |  | ✓ | ✓ |
| Convidar e revogar acessos ao portal da contratada | `documentos:gerenciar:portal_contratada` |  |  | ✓ | ✓ |
| Criar plano de ação a partir de um documento | `documentos:criar:plano_acao` |  |  | ✓ | ✓ |
| Criar tipos de documento | `documentos:criar:tipo_documento` |  |  | ✓ | ✓ |
| Editar a matriz de exigência de documentos e tipos de serviço | `documentos:editar:exigencia` |  |  | ✓ | ✓ |
| Editar alertas e política de bloqueio documental | `documentos:editar:configuracao` |  |  | ✓ | ✓ |
| Editar tipos de documento | `documentos:editar:tipo_documento` |  |  | ✓ | ✓ |
| Enviar documentos e novas versões | `documentos:enviar:documento` |  | ✓ | ✓ | ✓ |
| Inativar documentos | `documentos:inativar:documento` |  |  | ✓ | ✓ |
| Inativar tipos de documento | `documentos:inativar:tipo_documento` |  |  | ✓ | ✓ |
| Solicitar liberação excepcional de titular irregular | `documentos:solicitar:liberacao` |  | ✓ | ✓ | ✓ |
| Visualizar a matriz de exigência de documentos | `documentos:visualizar:exigencia` | ✓ | ✓ | ✓ | ✓ |
| Visualizar documentos e situação documental | `documentos:visualizar:documento` | ✓ | ✓ | ✓ | ✓ |
| Visualizar tipos de documento | `documentos:visualizar:tipo_documento` | ✓ | ✓ | ✓ | ✓ |

</details>

<details>

<summary>Gestão de EPIs (67)</summary>

| Permissão | Chave | Operador | Supervisor | Gestor | Administrador |
| --- | --- | :-: | :-: | :-: | :-: |
| Adicionar, editar e aprovar orçamentos de itens da solicitação de compra | `epis:orcar:solicitacao_compra` |  | ✓ | ✓ | ✓ |
| Anexar e remover arquivos em solicitações de compra | `epis:anexar:solicitacao_compra` |  | ✓ | ✓ | ✓ |
| Aprovar item de transferência | `epis:aprovar:item_transferencia` |  |  | ✓ | ✓ |
| Aprovar solicitações de EPI | `epis:aprovar:solicitacao` |  | ✓ | ✓ | ✓ |
| Aprovar solicitações de compra | `epis:aprovar:solicitacao_compra` |  | ✓ | ✓ | ✓ |
| Associar EPIs aos GHEs | `epis:associar:ghe_epi` |  |  | ✓ | ✓ |
| Associar item de solicitação a centro de custo | `epis:associar:item_centro_custo` | ✓ | ✓ | ✓ | ✓ |
| Cadastrar EPIs NR-6 customizados | `epis:criar:epi_configuracao` |  |  | ✓ | ✓ |
| Cadastrar Grupos Homogêneos de Exposição | `epis:criar:ghe` |  |  | ✓ | ✓ |
| Cadastrar fabricantes de EPI | `epis:criar:fabricante` |  |  | ✓ | ✓ |
| Cadastrar grupo de itens/CAs com soma de estoque | `epis:criar:grupo_estoque` |  |  | ✓ | ✓ |
| Cadastrar lavanderias | `epis:criar:lavanderia` |  |  | ✓ | ✓ |
| Cadastrar novos itens de EPI | `epis:criar:item_epi` |  |  | ✓ | ✓ |
| Cadastrar riscos ocupacionais | `epis:criar:risco_ocupacional` |  |  | ✓ | ✓ |
| Cancelar solicitação de transferência | `epis:cancelar:solicitacao_transferencia` |  | ✓ | ✓ | ✓ |
| Cancelar solicitações de compra | `epis:cancelar:solicitacao_compra` | ✓ | ✓ | ✓ | ✓ |
| Configurar emails para notificações de compra | `epis:configurar:emails_notificacao_compra` |  |  | ✓ | ✓ |
| Criar compra vinculada a item de transferência | `epis:solicitar_compra:por_item_transferencia` |  |  | ✓ | ✓ |
| Criar novos motivos de EPI | `epis:criar:motivo` |  |  | ✓ | ✓ |
| Criar solicitação de transferência de EPI | `epis:criar:solicitacao_transferencia` |  | ✓ | ✓ | ✓ |
| Criar solicitações de compra de EPIs | `epis:criar:solicitacao_compra` | ✓ | ✓ | ✓ | ✓ |
| Editar GHEs | `epis:editar:ghe` |  |  | ✓ | ✓ |
| Editar dados de fabricantes | `epis:editar:fabricante` |  |  | ✓ | ✓ |
| Editar grupo de itens/CAs com soma de estoque | `epis:editar:grupo_estoque` |  |  | ✓ | ✓ |
| Editar item de solicitação de transferência | `epis:editar:solicitacao_transferencia` |  |  | ✓ | ✓ |
| Editar itens de EPI existentes | `epis:editar:item_epi` |  |  | ✓ | ✓ |
| Editar lavanderias | `epis:editar:lavanderia` |  |  | ✓ | ✓ |
| Editar riscos ocupacionais | `epis:editar:risco_ocupacional` |  |  | ✓ | ✓ |
| Editar solicitações de compra pendentes | `epis:editar:solicitacao_compra` | ✓ | ✓ | ✓ | ✓ |
| Gerenciar estoque de EPIs | `epis:gerenciar:estoque` |  |  |  | ✓ |
| Inativar EPIs NR-6 customizados | `epis:inativar:epi_configuracao` |  |  | ✓ | ✓ |
| Inativar GHEs | `epis:inativar:ghe` |  |  | ✓ | ✓ |
| Inativar fabricantes | `epis:inativar:fabricante` |  |  | ✓ | ✓ |
| Inativar grupo de itens/CAs com soma de estoque | `epis:inativar:grupo_estoque` |  |  | ✓ | ✓ |
| Inativar itens de EPI | `epis:inativar:item_epi` |  |  | ✓ | ✓ |
| Inativar lavanderias | `epis:inativar:lavanderia` |  |  | ✓ | ✓ |
| Inativar motivos de EPI | `epis:inativar:motivo` |  |  | ✓ | ✓ |
| Inativar riscos ocupacionais | `epis:inativar:risco_ocupacional` |  |  | ✓ | ✓ |
| Marcar solicitação como processada | `epis:processar:solicitacao_compra` |  |  | ✓ | ✓ |
| Notificar em massa colaboradores com assinatura de EPI pendente | `epis:notificar:assinatura` |  | ✓ | ✓ | ✓ |
| Processar devolução de EPIs | `epis:devolver:epi` |  | ✓ | ✓ | ✓ |
| Processar item de transferência (mover estoque) | `epis:processar:item_transferencia` |  |  | ✓ | ✓ |
| Reenviar email de solicitação de compra | `epis:reenviar:email_solicitacao_compra` |  | ✓ | ✓ | ✓ |
| Registrar entrega de EPIs | `epis:entregar:epi` |  | ✓ | ✓ | ✓ |
| Registrar envio de EPI por correio | `epis:registrar:envio_correio` |  | ✓ | ✓ | ✓ |
| Rejeitar item de transferência | `epis:rejeitar:item_transferencia` |  |  | ✓ | ✓ |
| Rejeitar solicitações de EPI | `epis:rejeitar:solicitacao` |  | ✓ | ✓ | ✓ |
| Rejeitar solicitações de compra | `epis:rejeitar:solicitacao_compra` |  | ✓ | ✓ | ✓ |
| Solicitar EPIs | `epis:solicitar:epi` | ✓ | ✓ | ✓ | ✓ |
| Ver estoque em todas as unidades para análise | `epis:visualizar:estoque_todas_unidades` |  |  | ✓ | ✓ |
| Vincular/desvincular compras em solicitação de transferência | `epis:gerenciar:solicitacao_transferencia` |  |  | ✓ | ✓ |
| Visualizar GHEs | `epis:visualizar:ghe` |  |  | ✓ | ✓ |
| Visualizar estoque de EPIs | `epis:visualizar:estoque` |  | ✓ | ✓ | ✓ |
| Visualizar grupo de itens/CAs com soma de estoque | `epis:visualizar:grupo_estoque` | ✓ | ✓ | ✓ | ✓ |
| Visualizar lavanderias | `epis:visualizar:lavanderia` | ✓ | ✓ | ✓ | ✓ |
| Visualizar lista de fabricantes | `epis:visualizar:fabricante` | ✓ | ✓ | ✓ | ✓ |
| Visualizar o custo unitário dos itens | `epis:visualizar:custo_item` |  |  | ✓ | ✓ |
| Visualizar solicitações de compra de EPIs | `epis:visualizar:solicitacao_compra` | ✓ | ✓ | ✓ | ✓ |
| Visualizar solicitações de transferência | `epis:visualizar:solicitacao_transferencia` |  | ✓ | ✓ | ✓ |
| Visualizar todas as solicitações de compra | `epis:visualizar:todas_solicitacoes_compra` |  | ✓ | ✓ | ✓ |
| Visualizar todas as solicitações de transferência | `epis:visualizar:todas_solicitacoes_transferencia` |  |  | ✓ | ✓ |
| Visualizar todos os EPIs NR-6 customizados | `epis:visualizar:todos_epi_configuracao` |  |  | ✓ | ✓ |
| Visualizar todos os GHEs | `epis:visualizar:todos_ghe` |  |  | ✓ | ✓ |
| Visualizar todos os estoques de EPIs | `epis:visualizar:geral_estoque` |  |  | ✓ | ✓ |
| Visualizar todos os fabricantes | `epis:visualizar:todos_fabricante` |  |  | ✓ | ✓ |
| Visualizar todos os motivos de EPI | `epis:visualizar:todos_motivos` |  |  | ✓ | ✓ |
| Visualizar todos os riscos ocupacionais | `epis:visualizar:todos_risco_ocupacional` |  |  | ✓ | ✓ |

</details>

<details>

<summary>Gestão de Treinamentos (75)</summary>

| Permissão | Chave | Operador | Supervisor | Gestor | Administrador |
| --- | --- | :-: | :-: | :-: | :-: |
| Anexar certificado manualmente ao colaborador | `treinamentos:criar:certificado` |  | ✓ | ✓ | ✓ |
| Anexar documentos às turmas | `treinamentos:anexar:documento` |  | ✓ | ✓ | ✓ |
| Aprovar o plano anual de treinamentos | `treinamentos:aprovar:plano_anual` |  |  | ✓ | ✓ |
| Assinar certificados digitalmente (sem efeito no sistema hoje) | `treinamentos:assinar:certificado` |  |  | ✓ | ✓ |
| Associar treinamentos obrigatórios a GHEs | `treinamentos:associar:ghe_treinamento` |  |  | ✓ | ✓ |
| Cadastrar novos instrutores | `treinamentos:criar:instrutor` |  |  | ✓ | ✓ |
| Cadastrar novos treinamentos/cursos | `treinamentos:criar:treinamento` |  |  | ✓ | ✓ |
| Cancelar matrículas | `treinamentos:cancelar:matricula` |  |  | ✓ | ✓ |
| Cancelar turmas de treinamento (sem efeito no sistema hoje) | `treinamentos:cancelar:turma` |  |  | ✓ | ✓ |
| Coletar assinatura digital de treinandos | `treinamentos:coletar:assinatura_treinando` | ✓ | ✓ | ✓ | ✓ |
| Configurar alertas de vencimento | `treinamentos:configurar:alertas` |  | ✓ | ✓ | ✓ |
| Configurar as regras do módulo de Treinamentos (aproveitamento, EAD) | `treinamentos:configurar:modulo` |  | ✓ | ✓ | ✓ |
| Configurar periodicidade de reciclagem por GHE | `treinamentos:configurar:periodicidade_ghe` |  |  | ✓ | ✓ |
| Configurar renovação automática | `treinamentos:configurar:renovacao` |  |  | ✓ | ✓ |
| Criar categorias de treinamento | `treinamentos:criar:categoria_treinamento` |  |  | ✓ | ✓ |
| Criar e editar questionários de reação e de prova | `treinamentos:gerenciar:questionario` |  | ✓ | ✓ | ✓ |
| Criar instituições certificadoras | `treinamentos:criar:instituicao_certificadora` |  |  | ✓ | ✓ |
| Criar tipos de instituição | `treinamentos:criar:tipo_instituicao` |  |  | ✓ | ✓ |
| Criar turmas de treinamento (sem efeito no sistema hoje) | `treinamentos:criar:turma` |  | ✓ | ✓ | ✓ |
| Deletar documentos anexados | `treinamentos:deletar:documento` |  |  | ✓ | ✓ |
| Editar associações GHE-Treinamento | `treinamentos:editar:ghe_treinamento` |  |  | ✓ | ✓ |
| Editar categorias de treinamento | `treinamentos:editar:categoria_treinamento` |  |  | ✓ | ✓ |
| Editar dados de instrutores | `treinamentos:editar:instrutor` |  |  | ✓ | ✓ |
| Editar dados de treinamentos | `treinamentos:editar:treinamento` |  |  | ✓ | ✓ |
| Editar instituições certificadoras | `treinamentos:editar:instituicao_certificadora` |  |  | ✓ | ✓ |
| Editar matrículas | `treinamentos:editar:matricula` |  | ✓ | ✓ | ✓ |
| Editar tipos de instituição | `treinamentos:editar:tipo_instituicao` |  |  | ✓ | ✓ |
| Editar turmas de treinamento | `treinamentos:editar:turma` |  | ✓ | ✓ | ✓ |
| Enviar e organizar os vídeos e materiais do EAD | `treinamentos:gerenciar:conteudo_ead` |  | ✓ | ✓ | ✓ |
| Enviar notificações manuais | `treinamentos:enviar:notificacao` |  |  | ✓ | ✓ |
| Exportar pacote para fiscalização (ZIP) | `treinamentos:exportar:pacote_fiscalizacao` |  |  | ✓ | ✓ |
| Filtrar certificados vencidos/vencendo | `treinamentos:filtrar:vencimentos` |  |  | ✓ | ✓ |
| Finalizar turmas de treinamento | `treinamentos:finalizar:turma` |  |  | ✓ | ✓ |
| Gerar certificados de conclusão (sem efeito no sistema hoje) | `treinamentos:gerar:certificado` |  |  | ✓ | ✓ |
| Gerar listas de presença | `treinamentos:gerar:lista_presenca` |  | ✓ | ✓ | ✓ |
| Gerar relatórios de certificados | `treinamentos:gerar:relatorio_certificados` |  |  | ✓ | ✓ |
| Gerar relatórios de conformidade por setor/NR | `treinamentos:gerar:relatorio_conformidade` |  |  | ✓ | ✓ |
| Gerar relatórios de participação | `treinamentos:gerar:relatorio_participacao` |  | ✓ | ✓ | ✓ |
| Gerar relatórios de vencimentos | `treinamentos:gerar:relatorio_vencimentos` |  |  | ✓ | ✓ |
| Gerenciar qualificações de instrutores | `treinamentos:gerenciar:qualificacao_instrutor` |  |  | ✓ | ✓ |
| Inativar categorias de treinamento | `treinamentos:inativar:categoria_treinamento` |  |  |  | ✓ |
| Inativar instituições certificadoras | `treinamentos:inativar:instituicao_certificadora` |  |  |  | ✓ |
| Inativar instrutores | `treinamentos:inativar:instrutor` |  |  | ✓ | ✓ |
| Inativar tipos de instituição | `treinamentos:inativar:tipo_instituicao` |  |  |  | ✓ |
| Inativar treinamentos | `treinamentos:inativar:treinamento` |  |  | ✓ | ✓ |
| Invalidar certificados | `treinamentos:invalidar:certificado` |  |  |  | ✓ |
| Matricular funcionários em treinamentos | `treinamentos:criar:matricula` |  | ✓ | ✓ | ✓ |
| Montar o plano anual de treinamentos e o orçamento | `treinamentos:gerenciar:plano_anual` |  | ✓ | ✓ | ✓ |
| Reemitir certificados (sem efeito no sistema hoje) | `treinamentos:reemitir:certificado` |  |  | ✓ | ✓ |
| Registrar a avaliação de eficácia do treinamento | `treinamentos:avaliar:eficacia` |  | ✓ | ✓ | ✓ |
| Registrar aproveitamento de treinamento (NR-1 1.7.6 e 1.7.7) | `treinamentos:criar:aproveitamento` |  | ✓ | ✓ | ✓ |
| Registrar assinatura digital do instrutor (sem efeito no sistema hoje) | `treinamentos:assinar:turma_instrutor` |  | ✓ | ✓ | ✓ |
| Registrar presença em treinamentos | `treinamentos:registrar:presenca` |  | ✓ | ✓ | ✓ |
| Validar credenciais de instrutores | `treinamentos:validar:credencial_instrutor` |  |  | ✓ | ✓ |
| Ver a análise de vídeo e o rastreio dos colaboradores no EAD | `treinamentos:visualizar:analise_ead` |  | ✓ | ✓ | ✓ |
| Visualizar alertas e notificações | `treinamentos:visualizar:alertas` |  | ✓ | ✓ | ✓ |
| Visualizar carteirinha digital de certificados | `treinamentos:visualizar:carteirinha_digital` | ✓ | ✓ | ✓ | ✓ |
| Visualizar categorias de treinamento | `treinamentos:visualizar:categoria_treinamento` | ✓ | ✓ | ✓ | ✓ |
| Visualizar certificados | `treinamentos:visualizar:certificado` | ✓ | ✓ | ✓ | ✓ |
| Visualizar dashboard de validades | `treinamentos:visualizar:dashboard_validades` |  | ✓ | ✓ | ✓ |
| Visualizar documentos anexados | `treinamentos:visualizar:documento` |  | ✓ | ✓ | ✓ |
| Visualizar histórico de treinamentos por funcionário | `treinamentos:visualizar:historico_funcionario` | ✓ | ✓ | ✓ | ✓ |
| Visualizar indicadores gerenciais | `treinamentos:visualizar:indicadores` |  |  | ✓ | ✓ |
| Visualizar instituições certificadoras | `treinamentos:visualizar:instituicao_certificadora` | ✓ | ✓ | ✓ | ✓ |
| Visualizar lista de instrutores | `treinamentos:visualizar:instrutor` |  | ✓ | ✓ | ✓ |
| Visualizar matrículas | `treinamentos:visualizar:matricula` | ✓ | ✓ | ✓ | ✓ |
| Visualizar percentual de conformidade | `treinamentos:visualizar:conformidade` |  |  | ✓ | ✓ |
| Visualizar tipos de instituição | `treinamentos:visualizar:tipo_instituicao` | ✓ | ✓ | ✓ | ✓ |
| Visualizar todas as turmas | `treinamentos:visualizar:todos_turma` |  |  | ✓ | ✓ |
| Visualizar todos os certificados | `treinamentos:visualizar:todos_certificado` |  |  | ✓ | ✓ |
| Visualizar todos os instrutores | `treinamentos:visualizar:todos_instrutor` |  |  | ✓ | ✓ |
| Visualizar todos os treinamentos | `treinamentos:visualizar:todos_treinamento` |  |  | ✓ | ✓ |
| Visualizar treinamentos | `treinamentos:visualizar:treinamento` |  | ✓ | ✓ | ✓ |
| Visualizar treinamentos obrigatórios por GHE | `treinamentos:visualizar:ghe_treinamento` |  |  | ✓ | ✓ |
| Visualizar turmas de treinamento | `treinamentos:visualizar:turma` | ✓ | ✓ | ✓ | ✓ |

</details>

<details>

<summary>Planos de ação (8)</summary>

| Permissão | Chave | Operador | Supervisor | Gestor | Administrador |
| --- | --- | :-: | :-: | :-: | :-: |
| Atribuir itens de plano de ação | `planos_acao:atribuir:item_plano_acao` | ✓ | ✓ | ✓ | ✓ |
| Criar planos de ação internos | `planos_acao:criar:plano_acao` | ✓ | ✓ | ✓ | ✓ |
| Editar itens de plano de ação | `planos_acao:editar:item_plano_acao` | ✓ | ✓ | ✓ | ✓ |
| Editar planos de ação | `planos_acao:editar:plano_acao` | ✓ | ✓ | ✓ | ✓ |
| Listar planos de ação | `planos_acao:listar:planos_acao` | ✓ | ✓ | ✓ | ✓ |
| Visualizar detalhes de planos de ação | `planos_acao:visualizar:plano_acao` | ✓ | ✓ | ✓ | ✓ |
| Visualizar todos os itens de planos de ação | `planos_acao:visualizar:todos_itens_plano_acao` | ✓ | ✓ | ✓ | ✓ |
| Visualizar todos os planos de ação da empresa | `planos_acao:visualizar:todos_planos_acao` | ✓ | ✓ | ✓ | ✓ |

</details>

<details>

<summary>Relatórios (13)</summary>

| Permissão | Chave | Operador | Supervisor | Gestor | Administrador |
| --- | --- | :-: | :-: | :-: | :-: |
| Gerar e exportar os relatórios da Gestão de Acidentes | `relatorios:gerar:acidentes` |  | ✓ | ✓ | ✓ |
| Gerar relatórios da gestão de documentos (PDF e Excel) | `relatorios:gerar:documentos` |  | ✓ | ✓ | ✓ |
| Gerar relatórios de assinatura de EPIs | `relatorios:gerar:epi_assinatura` |  |  | ✓ | ✓ |
| Gerar relatórios de devolução de EPIs | `relatorios:gerar:epi_devolucao` |  |  | ✓ | ✓ |
| Gerar relatórios de formularios para Excel | `relatorios:gerar:formulario-excel` |  |  | ✓ | ✓ |
| Gerar relatórios de formularios para PDF | `relatorios:gerar:formulario-pdf` |  |  | ✓ | ✓ |
| Gerar relatórios de inventário de EPIs | `relatorios:gerar:epi_inventario` |  |  | ✓ | ✓ |
| Visualizar dashboard principal | `relatorios:visualizar:auditoria-dashboard` |  | ✓ | ✓ | ✓ |
| Visualizar dashboard principal | `relatorios:visualizar:epi-dashboard` |  | ✓ | ✓ | ✓ |
| Visualizar dashboard principal | `relatorios:visualizar:formulario-dashboard` |  | ✓ | ✓ | ✓ |
| Visualizar o painel da CIPA | `relatorios:visualizar:painel_cipa` |  | ✓ | ✓ | ✓ |
| Visualizar o painel de acidentes e indicadores | `relatorios:visualizar:painel_acidentes` |  | ✓ | ✓ | ✓ |
| Visualizar o painel de gestão de documentos | `relatorios:visualizar:painel_documentos` |  | ✓ | ✓ | ✓ |

</details>

<details>

<summary>Suporte (5)</summary>

| Permissão | Chave | Operador | Supervisor | Gestor | Administrador |
| --- | --- | :-: | :-: | :-: | :-: |
| Abrir ticket de suporte | `suporte:criar:ticket` | ✓ | ✓ | ✓ | ✓ |
| Avaliar atendimento de ticket de suporte resolvido | `suporte:avaliar:ticket` | ✓ | ✓ | ✓ | ✓ |
| Fechar ou cancelar ticket de suporte | `suporte:fechar:ticket` | ✓ | ✓ | ✓ | ✓ |
| Responder/comentar em ticket de suporte | `suporte:comentar:ticket` | ✓ | ✓ | ✓ | ✓ |
| Visualizar tickets de suporte da empresa | `suporte:visualizar:ticket` | ✓ | ✓ | ✓ | ✓ |

</details>

<details>

<summary>Usuários (6)</summary>

| Permissão | Chave | Operador | Supervisor | Gestor | Administrador |
| --- | --- | :-: | :-: | :-: | :-: |
| Criar novos usuários no sistema | `usuarios:criar:usuario` |  |  |  | ✓ |
| Editar informações de usuários | `usuarios:editar:usuario` |  |  |  | ✓ |
| Gerenciar roles de usuários | `usuarios:gerenciar:roles` |  |  |  | ✓ |
| Inativar usuários do sistema | `usuarios:inativar:usuario` |  |  |  | ✓ |
| Reativar usuários inativos | `usuarios:reativar:usuario` |  |  |  | ✓ |
| Visualizar lista e detalhes de usuários | `usuarios:visualizar:usuario` |  |  | ✓ | ✓ |

</details>

<details>

<summary>eSocial (1)</summary>

| Permissão | Chave | Operador | Supervisor | Gestor | Administrador |
| --- | --- | :-: | :-: | :-: | :-: |
| Enviar o certificado digital e configurar a transmissão ao eSocial | `esocial:gerenciar:certificado` |  |  | ✓ | ✓ |

</details>

## Dúvidas comuns

<details>

<summary>Posso mudar o que está marcado para uma role padrão?</summary>

Não. Para ter outra combinação, [crie uma role](criar-role.md) a partir da padrão.

</details>

<details>

<summary>A pessoa tem duas roles. Qual vale?</summary>

As duas. As permissões se somam.

</details>
