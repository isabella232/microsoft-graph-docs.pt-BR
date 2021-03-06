---
title: tipo de recurso plannerCategoryDescriptions
description: 'O recurso **plannerCategoryDescriptions** representa os rótulos descritivos das categorias que foram definidas para um plano. Ele pertence ao objeto Plan details. Pode haver até 6 categorias definidas. '
localization_priority: Normal
author: TarkanSevilmis
ms.prod: planner
doc_type: resourcePageType
ms.openlocfilehash: 96aa53647b5efcfae891b2865bb5d5358f4d5048
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/18/2020
ms.locfileid: "48037504"
---
# <a name="plannercategorydescriptions-resource-type"></a>tipo de recurso plannerCategoryDescriptions

Namespace: microsoft.graph

O recurso **plannerCategoryDescriptions** representa os rótulos descritivos das categorias que foram definidas para um plano. Ele pertence ao objeto [Plan Details](plannerplandetails.md) . Pode haver até 6 categorias definidas. 


## <a name="properties"></a>Propriedades
| Propriedade     | Tipo   |Descrição|
|:---------------|:--------|:----------|
|category1|String|O rótulo associado à categoria 1|
|category2|String|O rótulo associado à categoria 2|
|category3|String|O rótulo associado à categoria 3|
|category4|String|O rótulo associado à categoria 4|
|category5|String|O rótulo associado à categoria 5|
|category6|String|O rótulo associado à categoria 6|

## <a name="json-representation"></a>Representação JSON
Veja a seguir uma representação JSON do recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.plannerCategoryDescriptions"
}-->

```json
{
  "category1": "String",
  "category2": "String",
  "category3": "String",
  "category4": "String",
  "category5": "String",
  "category6": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "plannerCategoryDescriptions resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

