---
title: tipo de recurso attributeMappingSource
description: Define como um valor deve ser extraído (ou transformado) a partir do objeto Source.
localization_priority: Normal
doc_type: resourcePageType
author: ArvindHarinder1
ms.prod: microsoft-identity-platform
ms.openlocfilehash: 8e290ae6a31b927acce27a691fad39bf00a00985
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/18/2020
ms.locfileid: "48078049"
---
# <a name="attributemappingsource-resource-type"></a>tipo de recurso attributeMappingSource

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Define como um valor deve ser extraído (ou transformado) a partir do objeto Source. Por exemplo, pode ser um valor simples de um determinado atributo no objeto Source ou pode ser uma expressão mais complexa de concatenação/extração/substituição de cadeia de caracteres com base em vários atributos de origem.

## <a name="properties"></a>Propriedades

| Propriedade              | Tipo                      | Descrição               |
|:----------------------|:--------------------------|:--------------------------|
|expressão             |Cadeia de caracteres                     |Representação de expressão equivalente deste objeto **attributeMappingSource** .|
|name                   |Cadeia de caracteres                     |Parâmetro Name da origem do mapeamento. Dependendo do valor da propriedade **Type** , isso pode ser o nome da função, o nome do atributo de origem ou um valor constante a ser usado. |
|parameters             |coleção [stringKeyAttributeMappingSourceValuePair](synchronization-stringkeyattributemappingsourcevaluepair.md) | Se este objeto representar uma função, lista os parâmetros da função. Os parâmetros consistem nos objetos **attributeMappingSource** , permitindo expressões complexas. Se **Type** não for `Function` , esta propriedade será NULL/matriz vazia. |
|tipo                   | Cadeia de caracteres                    |O tipo desta fonte de mapeamento de atributos. Os valores possíveis são: `Attribute`, `Constant`, `Function`. O padrão é `Attribute`.|

## <a name="json-representation"></a>Representação JSON

Veja a seguir uma representação JSON do recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.attributeMappingSource"
}-->

```json
{
  "expression": "String",
  "name": "String",
  "parameters": [{"@odata.type": "microsoft.graph.stringKeyAttributeMappingSourceValuePair"}],
  "type": "String"
}
```

## <a name="json-examples"></a>Exemplos de JSON

Atributo simples para mapeamento de atributos

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.attributeMappingSource"
}-->

```json
{
    "expression": "[mail]",
    "name": "mail",
    "type": "Attribute"
}
```

Expressão que extrai primeiro 8 caracteres do atributo Source

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.attributeMappingSource"
}-->

```json
 {
    "expression": "Mid([userPrincipalName], 1, 8)",
    "name": "Mid",
    "parameters": [
        {
            "key": "source",
            "value": {
                "expression": "[userPrincipalName]",
                "name": "userPrincipalName",
                "parameters": [],
                "type": "Attribute"
            }
        },
        {
            "key": "start",
            "value": {
                "expression": "\"1\"",
                "name": "1",
                "parameters": [],
                "type": "Constant"
            }
        },
        {
            "key": "length",
            "value": {
                "expression": "\"8\"",
                "name": "8",
                "parameters": [],
                "type": "Constant"
            }
        }
    ],
    "type": "Function"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "attributeMappingSource resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->


