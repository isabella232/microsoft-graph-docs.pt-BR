---
title: tipo de recurso chatMessageHostedContent
description: Um conteúdo hospedado em uma mensagem de chat
localization_priority: Normal
author: clearab
ms.prod: microsoft-teams
doc_type: resourcePageType
ms.openlocfilehash: aff1033a68f2e98b5ea5f1ca940a2be026ae18c0
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/18/2020
ms.locfileid: "48064266"
---
# <a name="chatmessagehostedcontent-resource-type"></a>tipo de recurso chatMessageHostedContent

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Representa o conteúdo de equipes hospedados em uma mensagem de chat, como imagens ou trechos de código.
[Anexos de arquivo](chatmessageattachment.md) não são conteúdo hospedado; Eles são armazenados no SharePoint ou no OneDrive.

## <a name="methods"></a>Métodos

| Método       | Tipo de retorno | Descrição |
|:-------------|:------------|:------------|
| [Listar chatMessageHostedContent](../api/chatmessage-list-chatmessagehostedcontents.md) | [chatMessageHostedContent](chatmessagehostedcontent.md) | Recupere a lista de **chatMessageHostedContent** para uma mensagem. |
| [Obter chatMessageHostedContent](../api/chatmessagehostedcontent-get.md) | [chatMessageHostedContent](chatmessagehostedcontent.md) | Leia as propriedades e os relacionamentos de um objeto **chatMessageHostedContent** . |

## <a name="properties"></a>Propriedades

| Propriedade     | Tipo        | Descrição |
|:-------------|:------------|:------------|
|id            |String       | Somente leitura. Representa o identificador de conteúdo hospedado da mensagem de chat.|
|contentBytes  |Edm.Binary   | Somente gravação. Ao lançar o novo conteúdo hospedado da mensagem de chat, representa os bytes da carga. Eles são representados como uma cadeia de caracteres base64Encoded.|
|contentType   |String       | Somente gravação. Ao lançar o novo conteúdo hospedado da mensagem de chat, representa o tipo de conteúdo, como image/png.|

### <a name="instance-attributes"></a>Atributos de instância

Atributos de instância são propriedades com comportamentos especiais.
Essas propriedades são temporárias e definem o comportamento que o serviço deve executar ou fornecer valores de propriedade de curto prazo, como uma URL de download para um item que expira.

| Nome da propriedade                     | Tipo   | Descrição
|:----------------------------------|:-------|:--------------------------------
| @microsoft. Graph. TemporaryId      | cadeia de caracteres | Somente gravação. Representa o TemporaryId do conteúdo hospedado durante a postagem de uma mensagem para fazer referência ao conteúdo hospedado no recurso **chat** que está sendo enviado.|

## <a name="relationships"></a>Relações

Nenhum

## <a name="json-representation"></a>Representação JSON

Veja a seguir uma representação JSON do recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.chatMessageHostedContent",
  "baseType": "",
  "keyProperty": "id"
}-->

```json
{
  "@microsoft.graph.temporaryId": "String (identifier)",
  "id": "String (identifier)",
  "contentBytes": "String (binary)",
  "contentType": "String"
}
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "chatMessageHostedContent resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->


