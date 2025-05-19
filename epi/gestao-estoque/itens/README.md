# Visão Geral de Itens

## Introdução

O módulo de Itens é o componente central da Gestão de Estoque no Sistema GNRX, permitindo o cadastro e gerenciamento de todos os tipos de Equipamentos de Proteção Individual (EPIs) e itens complementares utilizados na organização. Este módulo serve como base para todo o controle de inventário, solicitações e distribuição de equipamentos aos colaboradores.

![Visão Geral de Itens](../../../assets/images/visao-geral-itens.png)

## Função e Importância

O gerenciamento de itens permite:

- Manter um catálogo completo de EPIs disponíveis
- Registrar informações essenciais como Certificados de Aprovação (CA)
- Controlar prazos de validade e períodos de troca
- Definir características específicas através de variantes
- Facilitar a conformidade com a NR-6 e outras regulamentações

## Tipos de Itens Suportados

O sistema permite o cadastro de dois tipos principais de itens:

1. **Itens com CA**: EPIs certificados pelo Ministério do Trabalho, com número de CA válido
   - Equipamentos obrigatórios conforme a NR-6
   - Itens com certificação e prazo de validade
   - EPIs para proteção específica contra riscos ocupacionais

2. **Itens sem CA**: Equipamentos complementares sem certificação oficial
   - Uniformes e vestimentas profissionais
   - Acessórios e complementos não certificados
   - Itens de uso pessoal sem requisito de certificação

## Informações Gerenciadas

Para cada item cadastrado, o sistema armazena:

- **Dados básicos**: Nome, descrição, fabricante
- **Informações regulatórias**: Número do CA, validade, classificação NR-6
- **Controle de ciclo de vida**: Período de troca recomendado
- **Características específicas**: Através do sistema de variantes
- **Informações de estoque**: Quantidade disponível, em uso e total

## Integração com Outros Módulos

O cadastro de itens se relaciona diretamente com:

- **Lotes**: Para controle de entrada no estoque
- **Variantes**: Para gerenciamento de características específicas
- **Solicitações**: Para disponibilização de EPIs aos colaboradores
- **Relatórios**: Para análise e gestão do inventário

## Interface Principal

A tela de listagem de itens apresenta:

- **Total de itens cadastrados**: Contador no canto superior esquerdo
- **Botões de ação**: Para adicionar novos itens e exportar relatórios
- **Ferramentas de pesquisa**: Para localizar itens específicos
- **Tabela de itens**: Com colunas para as principais informações
- **Ações por item**: Opções para visualizar, editar ou inativar

## Próximos Passos

Para gerenciar efetivamente os itens no Sistema GNRX, consulte os seguintes guias:

- [Listar Itens](./listar-itens.md) - Como visualizar e filtrar itens cadastrados
- [Criar Item com CA](./criar-item-com-ca.md) - Como cadastrar EPIs certificados
- [Criar Item sem CA](./criar-item-sem-ca.md) - Como cadastrar itens complementares
- [Editar Item](./editar-item.md) - Como atualizar informações dos itens
- [Desativar Item](./desativar-item.md) - Como remover itens do catálogo ativo

---

*Última atualização: 18 de Maio de 2025*