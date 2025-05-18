# Vincular EPIs

Esta página explica como associar Equipamentos de Proteção Individual (EPIs) aos riscos de um Grupo Homogêneo de Exposição (GHE) no Sistema GNRX.

## Visão Geral

A vinculação de EPIs é o processo final na configuração de um GHE, onde são definidos quais equipamentos de proteção serão fornecidos para cada risco identificado. Esta etapa é crucial para garantir que os colaboradores recebam exatamente os EPIs necessários para sua proteção.

## Relação entre Riscos e EPIs

No Sistema GNRX, existe uma relação direta entre:
- Riscos ocupacionais identificados no GHE
- EPIs necessários para proteção contra esses riscos

O sistema já possui uma matriz de recomendação pré-configurada que sugere automaticamente os EPIs adequados para cada risco, baseada na NR-6 e boas práticas de segurança. Porém, estas sugestões podem e devem ser ajustadas conforme as necessidades específicas da empresa.

## Acessando a Vinculação de EPIs

Para vincular EPIs a um risco específico em um GHE:

1. No menu lateral, clique em **Estruturas**
2. Selecione **GHEs**
3. Localize e clique no GHE desejado para abrir seus detalhes
4. Selecione a aba **Riscos / EPIs**
5. Localize o risco para o qual deseja gerenciar os EPIs
6. Clique no botão **Ver EPIs** ao lado do risco

![Acesso a Vinculação de EPIs](../../../assets/images/acesso-vincular-epis.png)

## Interface de Seleção de EPIs

Ao clicar em "Ver EPIs" para um risco específico, o sistema exibirá a tela de seleção de EPIs:

![Interface de Seleção de EPIs](../../../assets/images/interface-selecao-epis.png)

### Componentes da Interface

1. **Cabeçalho**: Exibe o nome do risco para o qual os EPIs estão sendo selecionados
2. **Barra de Pesquisa**: Permite buscar EPIs específicos por nome ou características
3. **Opção "Mostrar selecionados"**: Filtra para exibir apenas os EPIs já associados ao risco
4. **Categorias de EPIs**: Organiza os equipamentos por tipo de proteção:
   - EPI PARA PROTEÇÃO DA CABEÇA
   - EPI PARA PROTEÇÃO DOS OLHOS E FACE
   - EPI PARA PROTEÇÃO AUDITIVA
   - EPI PARA PROTEÇÃO RESPIRATÓRIA
   - EPI PARA PROTEÇÃO DO TRONCO
   - EPI PARA PROTEÇÃO DOS MEMBROS SUPERIORES
   - EPI PARA PROTEÇÃO DOS MEMBROS INFERIORES
   - EPI PARA PROTEÇÃO DO CORPO INTEIRO
   - EPI PARA PROTEÇÃO CONTRA QUEDAS
   - OUTROS

5. **Botões de Ação**:
   - **Selecionar Todos**: Seleciona todos os EPIs de uma categoria
   - **Desmarcar Todos**: Remove todas as seleções de uma categoria
   - **Expandir Todos**: Mostra todos os EPIs disponíveis
   - **Salvar alterações**: Confirma as seleções feitas
   - **Cancelar**: Descarta as alterações e retorna à tela anterior

## Processo de Seleção de EPIs

### Visualizando EPIs Recomendados

Ao abrir a tela, o sistema já exibirá com marcações os EPIs automaticamente recomendados para o risco específico. Estes são baseados na matriz de risco-proteção pré-configurada.

### Ajustando a Seleção

1. Revise os EPIs pré-selecionados para confirmar sua adequação
2. Marque EPIs adicionais que sejam necessários para sua operação específica
3. Desmarque EPIs que não sejam aplicáveis ao seu contexto

### Usando as Ferramentas de Seleção Rápida

Para facilitar a seleção:
- Use **Selecionar Todos** para marcar todos os EPIs de uma categoria
- Use **Desmarcar Todos** para limpar todas as seleções de uma categoria
- Expanda e recolha categorias para melhor visualização
- Utilize a barra de pesquisa para localizar EPIs específicos

### Finalizando a Seleção

Após ajustar a seleção de EPIs:
1. Revise todas as escolhas para garantir que são adequadas
2. Clique em **Salvar alterações** para confirmar
3. O sistema retornará à tela de riscos, agora com os EPIs atualizados

## Considerações Importantes

### Seleção Baseada em Evidências Técnicas

A seleção de EPIs deve ser fundamentada em:
- Avaliações quantitativas e qualitativas dos riscos
- Especificações técnicas dos equipamentos
- Normas regulamentadoras aplicáveis
- Recomendações de especialistas em SST

### Especificidade vs. Generalidade

- **Seja específico**: Selecione apenas os EPIs realmente necessários para o risco
- **Evite excesso**: Muitos EPIs podem dificultar a adesão e o uso correto
- **Considere conforto**: EPIs mais confortáveis tendem a ter maior adesão
- **Avalie compatibilidade**: Certifique-se de que os EPIs selecionados podem ser usados simultaneamente

### Impacto da Seleção

A vinculação de EPIs determinará:
- Quais equipamentos serão disponibilizados para solicitação
- O que será exibido na Ficha de EPI Digital do colaborador
- Os itens verificados em auditorias de conformidade
- As estatísticas e análises de consumo

## Melhores Práticas

- **Consulte Especialistas**: Envolva técnicos e engenheiros de segurança na seleção
- **Verifique CAs**: Confirme se os EPIs selecionados possuem Certificados de Aprovação válidos
- **Considere Feedback**: Leve em conta o retorno dos colaboradores sobre os EPIs
- **Revise Periodicamente**: Atualize as seleções conforme novas tecnologias e alterações nos processos
- **Documente Justificativas**: Mantenha registro das razões para seleção ou exclusão de EPIs específicos

## Próximos Passos

Após vincular todos os EPIs necessários:

1. Retorne à tela principal do GHE para verificar a configuração completa
2. Associe [colaboradores](../colaboradores/README.md) ao GHE
3. Verifique a [disponibilidade em estoque](../../gestao-estoque/relatorios/estoque-atual.md) dos EPIs selecionados
4. Inicie [solicitações](../../solicitacoes/criar-solicitacao/nova-solicitacao.md) para os colaboradores do GHE

## Erros Comuns e Soluções

| Erro | Solução |
|------|---------|
| Seleção excessiva de EPIs | Analise criticamente a real necessidade de cada equipamento |
| EPIs incompatíveis entre si | Verifique a compatibilidade de uso simultâneo dos equipamentos |
| EPI necessário não disponível na lista | Verifique se o item precisa ser [cadastrado](../../gestao-estoque/itens/criar-item-com-ca.md) no sistema |
| Alterações não refletidas nas solicitações | Lembre-se que alterações afetam apenas novas solicitações, não as já realizadas |

---

*Última atualização: 16 de Maio de 2025*