# Assinatura Digital

Esta página descreve o processo de assinatura digital para confirmação de recebimento de EPIs no Sistema GNRX.

## Visão Geral

A assinatura digital é a etapa final do processo de entrega de EPIs, representando a confirmação formal de que o colaborador recebeu os equipamentos e está ciente de suas responsabilidades quanto ao uso e conservação.

O Sistema GNRX oferece duas modalidades de assinatura:
1. **Assinatura Digital Simples**: realizada diretamente na tela do dispositivo
2. **Assinatura com Reconhecimento Facial**: método avançado que utiliza biometria facial para autenticação

## Processo de Assinatura Digital Simples

### Pré-requisitos
- Solicitação com status "Em Entrega"
- Acesso a um dispositivo com tela sensível ao toque ou mouse

### Etapas do Processo

![Tela de Assinatura Digital](../../../assets/images/assinatura-digital-tela.png)

1. Após confirmar os itens na [entrega](../entrega/confirmar-entrega.md), clique em **Prosseguir para Assinatura**
2. O sistema exibirá o Termo de Responsabilidade com a lista detalhada dos EPIs entregues
3. Solicite que o colaborador leia o termo atentamente
4. No campo de assinatura:
   - Em dispositivos touch: o colaborador deve assinar diretamente na tela
   - Em computadores: o colaborador deve desenhar sua assinatura usando o mouse
5. Caso necessário, o colaborador pode limpar a assinatura e refazê-la clicando em **Limpar**
6. Após a assinatura, clique em **Confirmar Assinatura**
7. O sistema salvará a assinatura e finalizará o processo de entrega

## Validação Legal da Assinatura Digital

A assinatura digital simples possui validade legal com base nas seguintes características:

- Vinculação inequívoca ao documento eletrônico (Termo de Responsabilidade)
- Registro de data e hora preciso (timestamp)
- Identificação do dispositivo utilizado e endereço IP
- Associação ao login do colaborador (quando realizado via aplicativo)
- Armazenamento seguro e imutável no sistema

## Visualizando Registros de Assinatura

As assinaturas digitais ficam registradas em:

1. **Ficha de EPI Digital**: visível na seção de histórico do colaborador
2. **Detalhes da Solicitação**: acessível ao abrir os detalhes da solicitação específica
3. **Relatórios de Conformidade**: incluído automaticamente em relatórios de documentação legal

![Exemplo de Registro de Assinatura](../../../assets/images/registro-assinatura.png)

## Considerações Importantes

- A assinatura digital simples é adequada para ambientes onde não é possível implementar o reconhecimento facial
- Para maior segurança jurídica, recomenda-se utilizar preferencialmente a [Assinatura com Reconhecimento Facial](./assinatura-reconhecimento-facial.md)
- O colaborador deve estar consciente de que a assinatura digital tem o mesmo valor legal de uma assinatura manual em papel
- O texto do termo de responsabilidade pode ser personalizado nas configurações do sistema, mas deve sempre conter elementos obrigatórios por lei

## Solução de Problemas

| Problema | Solução |
|----------|---------|
| Tela de assinatura não responde ao toque | Verifique se o navegador tem permissão para utilizar entrada de toque |
| Assinatura com mouse muito imprecisa | Ofereça ao colaborador a opção de tentar novamente ou utilize um dispositivo com tela sensível ao toque |
| Erro ao salvar assinatura | Verifique a conexão com a internet e tente novamente |
| Colaborador recusa-se a assinar | Registre a recusa no sistema e notifique o departamento de segurança do trabalho |

## Conformidade Legal

A assinatura digital simples atende aos requisitos legais previstos na legislação brasileira, incluindo:

- Lei 14.063/2020 (Assinaturas Eletrônicas)
- Medida Provisória 2.200-2/2001 (Infraestrutura de Chaves Públicas)
- Requisitos da NR-6 para comprovação de entrega de EPIs

Para cenários de maior risco jurídico ou em funções críticas, recomenda-se complementar com a modalidade de reconhecimento facial.