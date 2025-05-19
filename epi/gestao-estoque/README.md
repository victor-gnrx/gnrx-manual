# Gestão de Estoque

## Visão Geral

O módulo de Gestão de Estoque do Sistema GNRX Gestão de EPI permite controlar todo o ciclo de vida dos Equipamentos de Proteção Individual, desde o cadastro inicial até o gerenciamento do inventário por lotes e itens individuais. Este módulo é fundamental para garantir a disponibilidade de EPIs, controlar validades e manter a conformidade legal.

![Gestão de Estoque](../../assets/images/gestao-estoque-overview.png)

## Funcionalidades Principais

O módulo de Gestão de Estoque oferece as seguintes funcionalidades:

1. **Cadastro de Itens**: Registro de EPIs com ou sem Certificado de Aprovação (CA)
2. **Controle de Estoque**: Acompanhamento de quantidades disponíveis, em uso e totais
3. **Gerenciamento de Lotes**: Controle por lote com rastreabilidade completa
4. **Inventário Detalhado**: Visualização individual de cada EPI no sistema
5. **Controle de Validade**: Monitoramento de datas de validade dos EPIs
6. **Períodos de Troca**: Configuração dos prazos de substituição recomendados
7. **Variantes de Produtos**: Gerenciamento de tamanhos, cores e outras características
8. **Geração de Relatórios**: Exportação de dados em diferentes formatos

## Estrutura e Organização

O estoque no Sistema GNRX é organizado em uma estrutura hierárquica:

```
Item (Tipo de EPI)
 └── Lotes (Grupos de itens adquiridos juntos)
      └── Itens Individuais (Unidades físicas específicas)
           └── Variantes (Tamanhos, cores, etc.)
```

Essa estrutura permite:
- Rastrear cada unidade de EPI individualmente
- Controlar a validade de forma precisa
- Associar cada item a um colaborador específico
- Gerenciar custos em diversos níveis

## Interface Principal

A interface principal de Gestão de Estoque exibe:

- **Total de itens cadastrados**: Quantidade de diferentes tipos de EPIs no sistema
- **Lista de itens**: Com detalhes de CA, validade, fabricante e situação
- **Filtros de pesquisa**: Para localização rápida de itens específicos
- **Ferramentas de exportação**: Para geração de relatórios em PDF

Cada item na lista apresenta informações importantes como:
- ID e nome do item
- Número do CA (quando aplicável)
- Data de validade
- Fabricante
- Tempo de troca recomendado
- Quantidade em estoque
- Situação (Ativo/Inativo)

## Benefícios da Gestão de Estoque

Um gerenciamento eficiente do estoque de EPIs proporciona:

- **Prevenção de desabastecimento**: Garantindo que todos os colaboradores tenham acesso aos EPIs necessários
- **Controle de custos**: Monitorando gastos e identificando oportunidades de economia
- **Conformidade legal**: Assegurando o fornecimento de EPIs com CA válido
- **Rastreabilidade**: Permitindo acompanhar o histórico completo de cada item
- **Gestão de validade**: Evitando o uso de equipamentos vencidos
- **Otimização de recursos**: Melhorando a distribuição e utilização dos equipamentos

## Componentes do Módulo

O módulo de Gestão de Estoque é composto por:

1. **Itens**: Cadastro e gerenciamento dos tipos de EPIs
2. **Variantes**: Configuração de características específicas por item
3. **Lotes**: Controle de grupos de itens adquiridos
4. **Relatórios**: Geração de relatórios e análises de estoque

## Próximos Passos

Para utilizar efetivamente o módulo de Gestão de Estoque, consulte os seguintes guias:

- [Visão Geral de Itens](./itens/README.md) - Como funciona o cadastro de itens
- [Listar Itens](./itens/listar-itens.md) - Como visualizar e filtrar itens cadastrados
- [Criar Item com CA](./itens/criar-item-com-ca.md) - Como cadastrar EPIs com Certificado de Aprovação
- [Criar Item sem CA](./itens/criar-item-sem-ca.md) - Como cadastrar itens complementares
- [Gerenciamento de Variantes](./variantes/README.md) - Como configurar tamanhos, cores e outras variações
- [Controle de Lotes](./lotes/README.md) - Como gerenciar lotes de EPIs
- [Relatórios de Estoque](./relatorios/README.md) - Como gerar análises e relatórios

---

*Última atualização: 18 de Maio de 2025*