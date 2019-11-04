---
title: tipo de recurso personInterest
description: tipo de recurso personInterest
localization_priority: Normal
author: kevinbellinger
ms.prod: people
doc_type: resourcePageType
ms.openlocfilehash: 05918edf82712d5253403ed63312eb941be14103
ms.sourcegitcommit: dd94c3a0f7663699825b6dbc119cdcef494cd130
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2019
ms.locfileid: "37949495"
---
# <a name="personinterest-resource-type"></a>tipo de recurso personInterest

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Fornece informações detalhadas sobre os interesses que o usuário tenha associado a si mesmos em vários serviços.

Herda de [Myfacet](itemfacet.md).

## <a name="methods"></a>Métodos

| Método       | Tipo de retorno | Descrição |
|:---------------------------------------------------|:------------------------------------|:------------------------------------------------------------|
| [Obter personInterest](../api/personinterest-get.md) | [personInterest](personinterest.md) | Leia as propriedades e os relacionamentos de um objeto **personInterest** . |
| [Atualizar personInterest](../api/personinterest-update.md)          | [personInterest](personinterest.md) | Atualizar um objeto **personInterest** .                               |
| [Excluir personInterest](../api/personinterest-delete.md)          | Nenhum                                | Excluir um objeto **personInterest** .                               |

## <a name="properties"></a>Propriedades

| Propriedade     | Tipo             | Descrição                                                                          |
|:-------------|:-----------------|:-------------------------------------------------------------------------------------|
|categories    |String collection | Contém categorias que um usuário associou aos juros (por exemplo, pessoal, recipies). |
|description   |String            | Contém uma descrição dos juros.                                              |
|displayName   |Cadeia de caracteres            | Contém um nome amigável para os juros.                                           |
|webUrl        |String            | Contém um link para uma página da Web ou recurso sobre os juros.                         |

## <a name="relationships"></a>Relações

Nenhum

## <a name="json-representation"></a>Representação JSON

Veja a seguir uma representação JSON do recurso. 

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.personInterest",
  "baseType": ""
}-->

```json
{
  "categories": ["String"],
  "description": "String",
  "displayName": "String",
  "webUrl": "String"
}
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "personInterest resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->