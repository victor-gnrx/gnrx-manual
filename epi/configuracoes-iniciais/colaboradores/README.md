---
icon: users
---

# Visão Geral

## Visão Geral

O módulo de Colaboradores é um componente central do Sistema GNRx Gestão de EPI, onde são cadastrados e gerenciados todos os funcionários que receberão Equipamentos de Proteção Individual. Este cadastro conecta pessoas a unidades, setores, cargos e, mais importante, a Grupos Homogêneos de Exposição (GHEs), que determinam quais EPIs devem ser fornecidos a cada colaborador.

<figure><img src="../../.gitbook/assets/image (5).png" alt=""><figcaption></figcaption></figure>

## Funcionalidades Principais

O módulo de Colaboradores permite:

* Cadastrar informações completas de cada funcionário
* Vincular colaboradores a unidades, setores e cargos específicos
* Associar colaboradores aos GHEs correspondentes aos seus riscos ocupacionais
* Visualizar o histórico completo de EPIs recebidos e devolvidos
* Controlar o status de atividade (ativo/inativo) dos funcionários
* Gerenciar acesso dos colaboradores ao App GNRx - Colaboradores através de PIN
* Monitorar custos de EPIs por colaborador

## Importância do Cadastro de Colaboradores

Um cadastro preciso e completo dos colaboradores é fundamental para:

* **Conformidade Legal**: Documenta adequadamente a entrega de EPIs conforme exigido pela NR-6
* **Rastreabilidade**: Permite acompanhar todo o histórico de EPIs de cada funcionário
* **Gestão Eficiente**: Facilita a distribuição correta dos equipamentos com base nos riscos
* **Controle de Custos**: Monitora os gastos com EPIs por colaborador, setor ou unidade
* **Auditoria**: Fornece dados precisos para fiscalizações e auditorias internas

## Estrutura Hierárquica

No Sistema GNRX, os colaboradores são posicionados dentro desta hierarquia:

```
Empresa
 └── Unidades (locais físicos)
      └── Setores (áreas funcionais)
           └── Colaboradores (pessoas)
                ├── Cargos (funções específicas)
                └── GHEs (grupos por exposição a riscos)
                     └── EPIs Necessários
```

Esta estrutura permite que cada colaborador seja corretamente posicionado na organização e receba os EPIs adequados aos riscos aos quais está exposto.

## Relação com GHEs e EPIs

**O GHE (Grupo Homogêneo de Exposição) é o elemento fundamental que define quais EPIs um colaborador deve receber.** Esta é a conexão mais importante no sistema, pois:

* Cada GHE está associado a riscos ocupacionais específicos
* Cada risco determina quais EPIs são necessários para proteção
* O colaborador herda a necessidade de EPIs ao ser vinculado a um GHE

Esta vinculação garante que:

1. O colaborador seja protegido adequadamente contra os riscos de sua atividade
2. A empresa mantenha conformidade com os requisitos legais
3. O gerenciamento de EPIs seja feito de forma estruturada e eficiente

## PIN de Acesso

Todo colaborador possui um PIN de acesso de 6 dígitos, que serve para:

* Autenticar o colaborador no App GNRx - Colaborador
* Confirmar o reconhecimneto facial na solicitacao de EPIs em tablets ou dispositivos móveis

## Módulos Relacionados

O cadastro de colaboradores se conecta diretamente com:

* **Unidades**: Define onde o colaborador está fisicamente alocado
* **Setores**: Agrupa colaboradores por áreas funcionais dentro das unidades
* **Cargos**: Estabelece a função específica exercida pelo colaborador
* **GHEs**: Determina os riscos e consequentes EPIs necessários
* **Solicitações**: Registra as entregas e devoluções de EPIs
* **Ficha de EPI Digital**: Mantém o histórico completo de cada colaborador

## Próximos Passos

Para gerenciar eficientemente os colaboradores no Sistema GNRX, consulte os seguintes guias:

* [Listar Colaboradores](listar-colaboradores.md) - Como visualizar e filtrar colaboradores cadastrados
* [Criar Colaborador](criar-colaborador.md) - Processo para adicionar um novo colaborador
* [Editar Colaborador](broken-reference) - Como atualizar informações cadastrais
* [Desativar Colaborador](desativar-colaborador.md) - Procedimento para inativar temporariamente um colaborador
* [Vincular Unidades](vincular-unidades.md) - Como associar colaboradores a unidades físicas
* [Vincular Setores](vincular-setores.md) - Como definir os setores de atuação
* [Vincular GHE](vincular-ghe.md) - **Como definir os Grupos Homogêneos de Exposição que determinam os EPIs**
* [Histórico do Colaborador](broken-reference) - Como consultar o histórico completo de EPIs

## Recomendações

Para uma gestão eficiente de colaboradores, considere:

* Manter o cadastro sempre atualizado, especialmente em caso de mudanças de função ou setor
* Garantir que todos os colaboradores estejam associados aos GHEs corretos
* Verificar regularmente a adequação dos EPIs fornecidos com base nas atividades reais
* Atualizar prontamente o status de colaboradores que se desligaram da empresa
* Revisar periodicamente os vínculos entre colaboradores, setores, cargos e GHEs

***

_Última atualização: 16 de Maio de 2025_
