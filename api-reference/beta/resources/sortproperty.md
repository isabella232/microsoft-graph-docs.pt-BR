---
title: tipo de recurso SortProperty
description: Oferece a opção de classificar os resultados da pesquisa.
localization_priority: Normal
author: nmoreau
ms.prod: search
doc_type: resourcePageType
ms.openlocfilehash: 1f1288b2dc9ec05fe8aaedb5871c3bda68714f90
ms.sourcegitcommit: b70ee16cdf24daaec923acc477b86dbf76f2422b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/22/2020
ms.locfileid: "48193832"
---
# <a name="sortproperty-resource-type"></a>tipo de recurso SortProperty

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Representa as opções de classificação para ordenar os resultados da pesquisa.

## <a name="properties"></a>Propriedades

| Propriedade     | Tipo        | Descrição |
|:-------------|:------------|:------------|
|nome|String|O nome da propriedade a ser classificada. Obrigatório.|
|isDescending|Booliano|`True` se a ordem de classificação for decrescente. O padrão é `false` , com a ordem de classificação como crescente. Opcional.|

## <a name="json-representation"></a>Representação JSON

Veja a seguir uma representação JSON do recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.sortProperty",
  "baseType": null
}-->

```json
{
  "name": "String",
  "isDescending": "true"
}
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "sortProperty resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->