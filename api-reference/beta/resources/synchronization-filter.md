---
title: tipo de recurso de filtro
description: Determina quais objetos devem ser provisionados para o aplicativo.
localization_priority: Normal
doc_type: resourcePageType
author: ArvindHarinder1
ms.prod: microsoft-identity-platform
ms.openlocfilehash: c61ade97a2dd1da823fc48763040e0ee29573362
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/18/2020
ms.locfileid: "48028991"
---
# <a name="filter-resource-type"></a>tipo de recurso de filtro

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Determina quais objetos devem ser provisionados para o aplicativo. Por exemplo, você pode querer provisionar apenas usuários que estão localizados nos EUA. Quando um filtro de escopo estiver presente, os objetos que não satisfaçam o filtro serão ignorados durante a sincronização.

O filtro faz parte do [mapeamento de objetos](synchronization-objectmapping.md). Ele consiste em vários conjuntos de grupos de filtro e cada grupo de filtro contém uma ou mais cláusulas. Um objeto é considerado no escopo do grupo (o grupo é avaliado como `true` ) somente se todas as cláusulas do grupo são avaliadas `true` .

Um objeto é considerado em escopo para o conjunto de grupos (o conjunto de grupos é avaliado como `true` ) se qualquer um dos grupos no conjunto for avaliado como `true` .

Para mais informações, consulte [provisionamento de aplicativo baseado em atributo com filtros de escopo](/azure/active-directory/active-directory-saas-scoping-filters)

## <a name="properties"></a>Propriedades
| Propriedade     | Tipo   |Descrição|
|:---------------|:--------|:----------|
|categoryFilterGroups|coleção de [filtro](synchronization-filtergroup.md)|`*Experimental*` Conjunto de grupos de filtro usado para decidir se o objeto fornecido pertence e deve ser processado como parte desse mapeamento de objeto. Um objeto é considerado no escopo *se qualquer um dos grupos na coleção for avaliado como `true` *.|
|grupos|coleção de [filtro](synchronization-filtergroup.md)|Conjunto de grupos de filtro usado para decidir se o objeto fornecido está no escopo para provisionamento. **Este é o filtro que deve ser usado na maioria dos casos**. Se um objeto usado para satisfazer esse filtro em um determinado momento e o objeto ou o filtro tiver sido alterado, de forma que o filtro não seja mais satisfeito, esse objeto * receberá o provisionamento ". Um objeto é considerado no escopo *se qualquer um dos grupos na coleção for avaliado como `true` *.|
|inputFilterGroups|coleção de [filtro](synchronization-filtergroup.md)|`*Experimental*` Conjunto de grupos de filtro usado para filtrar objetos no estágio inicial de lê-los a partir do diretório. Se um objeto não satisfizer este filtro, ele não será mais processado. Importante compreender é que, se um objeto usado para atender a esse filtro em um determinado momento e o objeto ou o filtro tiver sido alterado para que o filtro não seja mais satisfeito, esse objeto *não será obtido sem provisionamento*. Um objeto é considerado no escopo *se qualquer um dos grupos na coleção for avaliado como `true` *. |

## <a name="json-representation"></a>Representação JSON

Veja a seguir uma representação JSON do recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.filter"
}-->

```json
{
  "categoryFilterGroups": [{"@odata.type": "microsoft.graph.filterGroup"}],
  "groups": [{"@odata.type": "microsoft.graph.filterGroup"}],
  "inputFilterGroups": [{"@odata.type": "microsoft.graph.filterGroup"}]
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "filter resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->


