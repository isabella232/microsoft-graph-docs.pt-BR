---
title: tipo de recurso workbookCommentReply
description: Definição do tipo de recurso workbookCommentReply
localization_priority: Normal
author: grangeryy
ms.prod: excel
doc_type: resourcePageType
ms.openlocfilehash: 26c1862a05431f02149cb4ddbef9a8ab57449d37
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/18/2020
ms.locfileid: "48015152"
---
# <a name="workbookcommentreply-resource-type"></a>tipo de recurso workbookCommentReply

Namespace: microsoft.graph

Representa uma resposta a um comentário do Excel.

## <a name="methods"></a>Methods

| Método       | Tipo de retorno | Descrição |
|:-------------|:------------|:------------|
| [Listar workbookCommentReplies](../api/workbookcomment-list-replies.md) | coleção [workbookCommentReply](workbookcommentreply.md) | Recupere uma lista de objetos workbookcommentreply. |
| [Obter workbookCommentReply](../api/workbookcommentreply-get.md) | [workbookCommentReply](workbookcommentreply.md) | Leia as propriedades e os relacionamentos do objeto workbookCommentReply. |
| [Criar workbookCommentReply](../api/workbookcomment-post-replies.md) | [workbookCommentReply](workbookcommentreply.md) | Criar um novo workbookCommentReply. |
## <a name="properties"></a>Propriedades

| Propriedade     | Tipo        | Descrição |
|:-------------|:------------|:------------|
|content|Cadeia de caracteres|O conteúdo de uma resposta de comentário.|
|contentType|String|Indica o tipo da resposta de comentário.|
|id|String|Representa o identificador de comentário. Somente leitura.|


## <a name="relationships"></a>Relações

Nenhum

## <a name="json-representation"></a>Representação JSON

Veja a seguir uma representação JSON do recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.workbookCommentReply",
  "baseType": "",
  "keyProperty": "id"
}-->

```json
{
  "content": "String",
  "contentType": "String",
  "id": "String (identifier)"
}
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "workbookCommentReply resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

