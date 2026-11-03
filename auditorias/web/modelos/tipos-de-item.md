---
description: "Os tipos de resposta que um item do modelo customizado pode ter."
icon: shapes
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

# Escolher o tipo de item

**Para que serve:** escolher como o auditor responde cada item do [modelo customizado](../modelo-customizado.md).

{% hint style="info" %}
**Quem pode fazer:** Gestor ou Administrador, com a permissão de editar modelos.
{% endhint %}

## Os tipos

| Grupo | Tipo | O auditor... |
| --- | --- | --- |
| Avaliação | **Conformidade** | marca Conforme, Não conforme ou N/A. |
| Avaliação | **Peso/Nota** | dá uma nota numa escala que você define. |
| Avaliação | **Informação** | só lê. O item é informativo. |
| Texto | **Texto** | escreve uma linha. |
| Texto | **Texto Longo** | escreve várias linhas. |
| Números | **Número** | informa um valor, com unidade. |
| Números | **Temperatura** | informa a temperatura em °C. |
| Data e Hora | **Data**, **Hora** ou **Data e Hora** | escolhe a data, a hora ou as duas. |
| Seleção | **Única Opção** | escolhe uma opção. |
| Seleção | **Múltiplas Opções** | escolhe várias opções. |
| Mídia e Documentos | **Imagem** | envia uma foto. |
| Mídia e Documentos | **Documento** | envia um arquivo. |
| Mídia e Documentos | **Assinatura** | assina na tela. |
| Outros | **Localização GPS** | registra as coordenadas. |
| Outros | **Código de Barras** | lê ou digita um código de barras ou QR Code. |
| Outros | **Grupo** | responde os subitens do grupo. |

## O que dá para configurar

* **Conformidade:** a infração e o potencial de multa, pelo valor ou pelo tipo e nível da NR-28.
* **Número:** **Valor Mínimo**, **Valor Máximo**, **Unidade de Medida** e **Casas Decimais**.
* **Peso/Nota:** **Valor Mínimo** e **Valor Máximo**.
* **Única Opção** e **Múltiplas Opções:** as **Opções Disponíveis**.
* **Texto:** o **Máximo de Caracteres**.
* **Imagem** e **Documento:** o **Tamanho Máximo (MB)**, se aceita vários arquivos e os **Tipos de Arquivo Permitidos**.
* **Localização GPS:** **Obrigar GPS Atual**, **Permitir Seleção no Mapa** e o **Endereço de Referência**.

## Dúvidas comuns

<details>

<summary>Posso trocar o tipo depois?</summary>

Sim, enquanto o modelo estiver em **Rascunho** ou **Em Edição**. Clique no ícone de editar do item.

</details>

<details>

<summary>Como crio um subitem?</summary>

No item, clique em **Adicionar Subitem**.

</details>
