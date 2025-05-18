# Configurações Gerais

O módulo de Configurações Gerais permite personalizar e adaptar o Sistema GNRx de Gestão de EPI às necessidades específicas da sua organização, incluindo catálogos de referência, motivos de movimentação e outros parâmetros fundamentais.

## Visão Geral

As Configurações Gerais são compostas por diversos componentes que estabelecem as bases de funcionamento do sistema, permitindo adaptações às particularidades de cada empresa, setor de atuação e regulamentações aplicáveis.

![Painel de Configurações Gerais](../assets/images/painel-configuracoes-gerais.png)

## Componentes Principais

### Riscos Ocupacionais

Permite gerenciar o catálogo de riscos ocupacionais que serão associados aos GHEs. O sistema já vem com uma base de dados de riscos conforme a NR-6, mas permite personalização e adições específicas para a realidade da empresa.

[Saiba mais sobre Riscos Ocupacionais](./riscos/README.md)

### Catálogos de EPIs

O sistema possui um catálogo completo baseado na NR-6, que pode ser complementado com itens customizados específicos para a organização. Esta seção permite gerenciar tanto os itens padrão quanto os personalizados.

[Saiba mais sobre Catálogos de EPIs](./catalogos/README.md)

### Motivos de Movimentação

Permite configurar os motivos padronizados para diversas operações no sistema:
- Motivos de solicitação de EPIs
- Motivos de devolução
- Motivos de perda
- Motivos de quebra

[Saiba mais sobre Motivos](./motivos/README.md)

## Importância das Configurações Gerais

Configurar corretamente estes parâmetros é fundamental para:

1. **Padronização de Processos**: Garante consistência nas operações realizadas por diferentes usuários
2. **Análise de Dados**: Permite extrair relatórios e estatísticas com categorias padronizadas
3. **Conformidade Legal**: Assegura alinhamento com exigências regulatórias como a NR-6
4. **Eficiência Operacional**: Simplifica processos ao oferecer opções predefinidas padronizadas

## Configuração Inicial Recomendada

Ao implementar o Sistema GNRX, recomendamos a seguinte sequência para as Configurações Gerais:

1. Revisar e complementar o catálogo de riscos ocupacionais
2. Revisar e complementar o catálogo de EPIs
3. Configurar os motivos de movimentação adequados à realidade da empresa
4. Realizar testes de validação do fluxo completo

## Permissões de Acesso

O acesso às Configurações Gerais normalmente é restrito a perfis administrativos:

- Administradores do Sistema
- Gestores de Segurança do Trabalho
- Coordenadores de EPI

Outros perfis geralmente têm permissão apenas de visualização ou acesso restrito a áreas específicas.

## Impacto das Configurações

É importante ressaltar que alterações nas Configurações Gerais podem ter impacto significativo no funcionamento do sistema:

- Mudanças em catálogos podem afetar relatórios históricos
- Alterações em motivos podem impactar fluxos de trabalho estabelecidos
- Desativação de itens pode afetar GHEs e entregas programadas

Por isso, recomenda-se:
1. Planejar cuidadosamente as configurações iniciais
2. Documentar alterações significativas
3. Comunicar mudanças aos usuários do sistema
4. Realizar alterações preferencialmente em períodos de baixa utilização