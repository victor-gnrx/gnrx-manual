# Editar Risco Ocupacional

## Introdução

A funcionalidade de edição de riscos permite modificar as informações de riscos ocupacionais personalizados previamente criados pela empresa. Esta capacidade é importante para manter a base de dados atualizada conforme mudanças nos processos, novas descobertas ou ajustes na terminologia utilizada pela organização.

![Interface de Edição de Risco](../../../assets/images/editar-risco.png)

## Limitações Importantes

**Atenção**: Conforme mencionado anteriormente, apenas riscos personalizados (criados pela própria empresa) podem ser editados. Os riscos pré-configurados do sistema base não permitem edição para garantir a integridade e conformidade do GNRX com as normas regulamentadoras.

## Como Acessar

Para editar um risco ocupacional personalizado:

1. Acesse o menu **Configurações** na barra de navegação principal
2. Selecione a opção **Riscos** no submenu que se abre
3. Localize o risco personalizado que deseja editar na lista
4. Clique no ícone de edição (lápis) na coluna "Opções" do risco desejado

Se o ícone de edição não estiver disponível, isto indica que o risco faz parte da base pré-configurada e não pode ser editado.

## Formulário de Edição de Risco

O modal de edição de risco apresenta os mesmos campos do formulário de criação, preenchidos com os dados atuais:

### Campos Editáveis

- **Nome**: Denominação do risco
  - Campo de texto com limite de 100 caracteres
  - Deve permanecer único no sistema

- **Descrição**: Detalhamento sobre o risco, suas características e consequências
  - Campo de texto com limite de 500 caracteres
  - Pode ser expandido para incluir novas informações relevantes

- **Categoria**: Classificação do risco conforme sua natureza
  - Campo de seleção com as opções:
    - Riscos físicos
    - Riscos químicos
    - Riscos biológicos
    - Riscos ergonômicos
    - Riscos de acidentes

### Botões de Ação

- **Salvar**: Confirma as alterações realizadas e atualiza o registro do risco
- **Cancelar**: Fecha o modal sem salvar as modificações, mantendo os dados originais

## Passo a Passo para Editar um Risco

### 1. Localizar o Risco

1. Utilize a funcionalidade de pesquisa para encontrar o risco desejado, se necessário
2. Verifique se o risco possui o ícone de edição na coluna "Opções"
3. Clique no ícone de edição para abrir o formulário

### 2. Realizar as Modificações

1. Altere os campos necessários:
   - Atualize o nome para uma denominação mais precisa, se necessário
   - Refine a descrição para incluir informações atualizadas
   - Reclassifique a categoria, se aplicável

2. Revise cuidadosamente as alterações antes de prosseguir

### 3. Confirmar as Alterações

1. Clique no botão **Salvar** para aplicar as modificações
2. Aguarde a mensagem de confirmação do sistema

## Impacto das Edições

Ao editar um risco ocupacional, é importante entender os impactos potenciais:

- **Associações existentes**: As alterações serão refletidas em todos os GHEs que utilizam este risco
- **Documentação histórica**: Registros anteriores manterão os dados no momento em que foram criados
- **Relatórios**: Novos relatórios utilizarão as informações atualizadas do risco

## Considerações Importantes

- **Mudanças substanciais**: Se as alterações modificarem completamente a natureza do risco, considere criar um novo risco em vez de editar
- **Consistência**: Mantenha a consistência com a nomenclatura e padrões utilizados nos demais riscos
- **Histórico**: O sistema mantém um registro de quando e por quem as alterações foram realizadas
- **Vinculos**: Verifique se as edições afetam a adequação dos EPIs vinculados ao risco

## Boas Práticas

Para editar riscos de forma eficaz:

- **Documentação**: Registre internamente os motivos das alterações realizadas
- **Comunicação**: Informe a equipe de saúde e segurança sobre modificações significativas
- **Revisão periódica**: Estabeleça uma rotina para revisar e atualizar os riscos cadastrados
- **Preservação da essência**: Ao editar, mantenha a essência original do risco para não invalidar associações existentes

## Próximos Passos

Após editar um risco, você pode:

- Revisar as associações do risco com GHEs e EPIs
- Verificar documentos e registros que utilizam o risco para garantir que permanecem adequados
- [Desativar Risco](./desativar-risco.md) - Caso o risco não seja mais aplicável

---

*Última atualização: 18 de Maio de 2025*