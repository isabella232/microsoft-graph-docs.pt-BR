---
title: tipo de recurso reviewset
description: Representa o conjunto estático de informações armazenadas eletronicamente coletadas para uso em litígio, investigação ou solicitação regulatória.
localization_priority: Normal
author: mahage-msft
ms.prod: compliance
doc_type: resourcePageType
ms.openlocfilehash: f1bf04c8357fbd57876b460848c549b3edd6f1f7
ms.sourcegitcommit: 7ceec757fd82ef3fd80aa3089ef46d3807aa3aa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2020
ms.locfileid: "48400736"
---
# <a name="reviewset-resource-type"></a>tipo de recurso reviewset

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Representa o conjunto estático de informações armazenadas eletronicamente coletadas para uso em litígio, investigação ou solicitação regulatória.

## <a name="methods"></a>Métodos

| Método       | Tipo de retorno | Descrição |
|:-------------|:------------|:------------|
| [List](../api/reviewset-list.md) | coleção [reviewset](reviewset.md) | Obter uma coleção de conjuntos de revisão. |
| [Get](../api/reviewset-get.md) | [reviewSet](reviewset.md) | Leia as propriedades e os relacionamentos de um objeto **reviewset** . |
| [Create](../api/reviewset-post.md) | [reviewSet](reviewset.md) | Criar um novo conjunto de revisão. |

## <a name="properties"></a>Propriedades

| Propriedade     | Tipo        | Descrição |
|:-------------|:------------|:------------|
|createdBy| [identitySet](/graph/api/resources/identityset) | O usuário que criou o conjunto de revisão. Somente leitura. |
|createdDateTime|DateTimeOffset| O DateTime quando o conjunto de revisão foi criado. O tipo Timestamp representa informações de data e hora usando o formato ISO 8601 e está sempre no horário UTC. Por exemplo, meia-noite em UTC no dia 1º de janeiro de 2014 teria esta aparência: `'2014-01-01T00:00:00Z'`. Somente leitura. |
|displayName|Cadeia de caracteres| O nome do conjunto de revisão. O nome é exclusivo com um limite máximo de 64 caracteres. |
|id|Cadeia de caracteres| O identificador exclusivo do conjunto de revisão. Somente leitura. |

## <a name="relationships"></a>Relações

| Relação | Tipo        | Descrição |
|:-------------|:------------|:------------|
| Analisar consulta de definição |coleção [reviewSetQuery](reviewsetquery.md)| Somente leitura. Anulável.|

## <a name="json-representation"></a>Representação JSON

Veja a seguir uma representação JSON do recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.reviewSet",
  "baseType": "",
  "keyProperty": "id"
}-->

```json
{
  "createdBy": {"@odata.type": "microsoft.graph.identitySet"},
  "createdDateTime": "String (timestamp)",
  "displayName": "String",
  "id": "String (identifier)"
}
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "reviewSet resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->