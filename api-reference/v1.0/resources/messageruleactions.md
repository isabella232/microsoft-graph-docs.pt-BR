---
title: Tipo de recurso messageRuleActions
description: Representa o conjunto de ações que estão disponíveis para uma regra.
author: svpsiva
localization_priority: Normal
ms.prod: outlook
doc_type: resourcePageType
ms.openlocfilehash: ed2486994a9ccb496dc92e241506baa867ebeb1f
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/18/2020
ms.locfileid: "47965383"
---
# <a name="messageruleactions-resource-type"></a>Tipo de recurso messageRuleActions

Namespace: microsoft.graph


Representa o conjunto de ações que estão disponíveis para uma regra.

## <a name="properties"></a>Propriedades
| Propriedade     | Tipo   |Descrição|
|:---------------|:--------|:----------|
| assignCategories | Coleção de cadeia de caracteres | Uma lista de categorias a serem atribuídas a uma mensagem. |
| copyToFolder | Cadeia de caracteres | O ID de uma pasta para a qual uma mensagem deve ser copiada. |
| delete | Boolean | Indica se uma mensagem deve ser movida para a pasta Itens Excluídos. |
| forwardAsAttachmentTo | Coleção [recipient](recipient.md) | Os endereços de email dos destinatários para os quais uma mensagem deve ser encaminhada como um anexo. |
| forwardTo | Coleção [recipient](recipient.md) | Os endereços de email dos destinatários para os quais uma mensagem deve ser encaminhada. |
| markAsRead | Boolean | Indica se uma mensagem deve ser marcada como lida. |
| markImportance | importância | Define a importância da mensagem, que pode ser: `low`, `normal`, `high`. |
| moveToFolder |  Cadeia de caracteres| O ID da pasta para a qual uma mensagem será movida. |
| permanentDelete | Boolean | Indica se uma mensagem deve ser excluída permanentemente e não salva na pasta Itens Excluídos. |
| redirectTo | Coleção [recipient](recipient.md) | Os endereços de email para os quais uma mensagem deve ser redirecionada. |
| stopProcessingRules | Boolean | Indica se regras subsequentes devem ser avaliadas. |

## <a name="json-representation"></a>Representação JSON
Veja a seguir uma representação JSON do recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [
   ],
  "@odata.type": "microsoft.graph.messageRuleActions"
}-->

```json
{
  "assignCategories": ["String"],
  "copyToFolder": "String",
  "delete": "Boolean",
  "forwardAsAttachmentTo": [{"@odata.type": "microsoft.graph.recipient"}],
  "forwardTo": [{"@odata.type": "microsoft.graph.recipient"}],
  "markAsRead": "Boolean",
  "markImportance": "String",
  "moveToFolder": "String",
  "permanentDelete": "Boolean",
  "redirectTo": [{"@odata.type": "microsoft.graph.recipient"}],
  "stopProcessingRules": "Boolean"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "messageRuleActions resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

