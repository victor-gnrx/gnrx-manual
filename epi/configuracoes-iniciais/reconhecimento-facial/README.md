# Reconhecimento Facial

## Visão Geral

O módulo de Reconhecimento Facial do Sistema GNRX Gestão de EPI oferece uma solução avançada para autenticação biométrica de colaboradores, garantindo segurança e rastreabilidade nas operações de entrega e devolução de Equipamentos de Proteção Individual.

![Reconhecimento Facial](../../../assets/images/reconhecimento-facial-overview.png)

### Importância do Reconhecimento Facial

A tecnologia de reconhecimento facial traz diversos benefícios operacionais e legais:

- **Segurança**: Garante que apenas o colaborador autorizado possa assinar pelo recebimento de EPIs
- **Conformidade Legal**: Fornece evidência biométrica para comprovar a entrega efetiva dos equipamentos
- **Eficiência**: Elimina a necessidade de assinaturas em papel e agiliza o processo de entrega
- **Auditoria**: Cria registros inalteráveis para fins de fiscalização e auditoria
- **Mobilidade**: Permite entregas e assinaturas em campo através de dispositivos móveis

### Casos de Uso Principais

O reconhecimento facial é utilizado principalmente para:

1. **Assinatura de recebimento de EPIs** - Confirma que o EPI foi entregue diretamente ao colaborador correto
2. **Registro de devolução** - Autentica a devolução de equipamentos reutilizáveis
3. **Acesso ao aplicativo móvel** - Alternativa segura ao PIN numérico para acesso ao app
4. **Registro de treinamentos** - Confirmação de presença em treinamentos de uso de EPIs

### Fluxo de Processo

```
Cadastro Inicial → Treinamento do Modelo → Validação → Uso em Operações Diárias → Atualização Periódica
```

### Considerações de Privacidade

O Sistema GNRX implementa as melhores práticas de privacidade e segurança para os dados biométricos:

- Dados criptografados em repouso e em trânsito
- Acesso aos dados biométricos restrito a funções essenciais
- Consentimento explícito do colaborador no cadastro
- Dados utilizados exclusivamente para finalidades específicas
- Conformidade com LGPD e outras legislações de privacidade aplicáveis

## Requisitos Técnicos

Para utilização adequada do reconhecimento facial, recomenda-se:

- Câmera frontal com resolução mínima de 2MP
- Iluminação adequada no ambiente de registro e verificação
- Conexão à internet estável (para sincronização)
- Dispositivos compatíveis: tablets, smartphones ou notebooks com webcam

## Indicadores Visuais

O sistema utiliza os seguintes indicadores para o status de reconhecimento facial:

| Status | Indicador | Significado |
|--------|-----------|-------------|
| Não cadastrado | Vermelho | O colaborador não possui reconhecimento facial cadastrado |
| Cadastrado | Verde | O colaborador possui reconhecimento facial ativo e validado |
| Em processamento | Amarelo | O cadastro está em andamento ou aguardando sincronização |
| Expirado | Laranja | O cadastro está desatualizado e precisa ser renovado |

## Fluxo de Implementação

A implementação completa do reconhecimento facial envolve três etapas principais:

1. [Cadastrar Face](./cadastrar-face.md) - Registro inicial da face do colaborador
2. [Atualizar Face](./atualizar-face.md) - Renovação periódica ou quando necessário

## Próximos Passos

Para implementar o reconhecimento facial em sua organização, consulte os seguintes guias:

- [Cadastrar Face](./cadastrar-face.md) - Como realizar o cadastro inicial
- [Atualizar Face](./atualizar-face.md) - Como atualizar o cadastro existente

---

*Última atualização: 18 de Maio de 2025*