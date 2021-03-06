---
title: Tipo de recurso referenceAttachment
description: Um link para um arquivo (como um arquivo de texto ou um documento do Word) em uma unidade de nuvem do OneDrive for Business ou outros locais de armazenamento compatíveis, anexado a um evento, mensagem ou postagem.
localization_priority: Normal
ms.prod: outlook
author: svpsiva
doc_type: resourcePageType
ms.openlocfilehash: e410e5b039a18e32e55058d3f33c0e75be52ee79
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/18/2020
ms.locfileid: "48072827"
---
# <a name="referenceattachment-resource-type"></a>Tipo de recurso referenceAttachment

Namespace: microsoft.graph

Um link para um arquivo (como um arquivo de texto ou um documento do Word) em uma unidade de nuvem do OneDrive for Business ou outros locais de armazenamento compatíveis, anexado a um evento, mensagem ou postagem.

Derivado de [attachment](attachment.md).

## <a name="methods"></a>Métodos

| Método       | Tipo de retorno  |Descrição|
|:---------------|:--------|:----------|
|[Get](../api/attachment-get.md) | [referenceAttachment](referenceattachment.md) |Leia as propriedades e os relacionamentos do objeto referenceAttachment.|
|[Delete](../api/attachment-delete.md) | Nenhum |Exclua o objeto referenceAttachment. |

## <a name="properties"></a>Propriedades
| Propriedade     | Tipo   |Descrição|
|:---------------|:--------|:----------|
|contentType|String|O tipo de conteúdo do anexo.|
|id|Cadeia de caracteres|A ID do anexo.  Somente leitura.|
|isInline|Booliano|Defina como verdadeiro se o anexo é exibido embutido no corpo do objeto de incorporação.|
|lastModifiedDateTime|DateTimeOffset|Data e hora em que o anexo foi modificado pela última vez. O tipo Timestamp representa informações de data e hora usando o formato ISO 8601 e está sempre no horário UTC. Por exemplo, meia-noite em UTC no dia 1º de janeiro de 2014 teria esta aparência: `'2014-01-01T00:00:00Z'`|
|nome|Cadeia de caracteres|O texto exibido abaixo do ícone que representa o anexo incorporado. Não precisa ser o nome real do arquivo.|
|size|Int32|O tamanho dos metadados, em bytes, que são armazenados na mensagem para o anexo. Esse valor não indica o tamanho real do arquivo.|

## <a name="relationships"></a>Relações
Nenhum



## <a name="json-representation"></a>Representação JSON

Veja a seguir uma representação JSON do recurso

<!--{
  "blockType": "resource",
  "optionalProperties": [],
  "baseType": "microsoft.graph.attachment",
  "keyProperty":"id",
  "@odata.type": "microsoft.graph.referenceAttachment"
}-->

```json
{
  "contentType": "string",
  "id": "string (identifier)",
  "isInline": true,
  "lastModifiedDateTime": "String (timestamp)",
  "name": "string",
  "size": 1024
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "referenceAttachment resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

