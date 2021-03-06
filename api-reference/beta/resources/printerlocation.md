---
title: tipo de recurso printerLocation
description: Representa o local físico e hierárquico de uma impressora.
author: braedenp-msft
localization_priority: Normal
ms.prod: universal-print
doc_type: resourcePageType
ms.openlocfilehash: 49b5221d31951ae35d72422dd4cb88ec254b4b82
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/18/2020
ms.locfileid: "48048824"
---
# <a name="printerlocation-resource-type"></a>tipo de recurso printerLocation

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Representa o local físico e hierárquico de uma impressora.

## <a name="properties"></a>Propriedades
| Propriedade     | Tipo        | Descrição |
|:-------------|:------------|:------------|
|latitude|Double|O Latitude em que a impressora está localizada.|
|longitude|Double|A longitude em que a impressora está localizada.|
|altitudeInMeters|Int32|A altitude, em metros, em que a impressora está localizada em.|
|streetAddress|String|O endereço de rua onde a impressora está localizada.|
|subunidade|Coleção de cadeias de caracteres|A hierarquia de subunidade onde a impressora está localizada. Os elementos devem estar em ordem hierárquica. Por exemplo, se um campus for dividido em seções diferentes, a hierarquia poderá ter a seguinte aparência: `["East Wing", "Block A"]`|
|city|Cadeia de caracteres|A cidade na qual a impressora está localizada.|
|postalCode|Cadeia de caracteres|O CEP em que a impressora está localizada.|
|countryOrRegion|String|O país ou a região em que a impressora está localizada.|
|site|Cadeia de caracteres|O site no qual a impressora está localizada.|
|Build|Cadeia de caracteres|O edifício em que a impressora está localizada.|
|floorNumber|Int32|O número do andar em que a impressora está localizada.|
|floorDescription|Cadeia de caracteres|A descrição do piso em que a impressora está localizada.|
|Númerodasala|Int32|O número da sala em que a impressora está localizada.|
|roomDescription|Cadeia de caracteres|A descrição da sala em que a impressora está localizada.|
|organization|Coleção de cadeias de caracteres|A hierarquia organizacional à qual a impressora pertence. Os elementos devem estar em ordem hierárquica.|
|subdivisão|Coleção de cadeias de caracteres|A subdivisão em que a impressora está localizada. Os elementos devem estar em ordem hierárquica.|
|stateOrProvince|Cadeia de caracteres|O estado ou província em que a impressora está localizada.|

## <a name="json-representation"></a>Representação JSON

Veja a seguir uma representação JSON do recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.printerLocation"
}-->

```json
{
    "latitude": 80.1,
    "longitude": -170.1,
    "altitudeInMeters": 123456,
    "streetAddress": "String",
    "subUnit": ["String"],
    "city": "String",
    "postalCode": "String",
    "countryOrRegion": "String",
    "site": "String",
    "building": "String",
    "floorNumber": 123456,
    "floorDescription": "String",
    "roomNumber": 123456,
    "roomDescription": "String",
    "organization": ["String"],
    "subdivision": ["String"],
    "stateOrProvince": "String"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "printerLocation resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

