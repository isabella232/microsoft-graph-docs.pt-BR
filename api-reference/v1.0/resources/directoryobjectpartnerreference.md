---
title: tipo de recurso directoryObjectPartnerReference
description: Representa uma referência a um objeto Directory em um locatário do parceiro. Herda do directoryObject.
author: keylimesoda
localization_priority: Normal
ms.prod: microsoft-identity-platform
doc_type: resourcePageType
ms.openlocfilehash: 39a3077862727f4d8457a6d0105f03296ba67950
ms.sourcegitcommit: 577bfd3bb8a2e2679ef1c5942a4a496c2aa3a277
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/17/2020
ms.locfileid: "48582153"
---
# <a name="directoryobjectpartnerreference-resource-type"></a>tipo de recurso directoryObjectPartnerReference

Namespace: microsoft.graph

Representa uma referência a um objeto Directory em uma organização parceira. Herda de [directoryObject](/graph/api/resources/directoryobject?view=graph-rest-v1.0).

## <a name="properties"></a>Propriedades

| Propriedade | Tipo | Descrição |
|:---------------|:--------|:----------|
|description|String| Descrição do objeto retornado. Somente leitura. |
|displayName|String| Nome do objeto de diretório que está sendo retornado, como o grupo ou o aplicativo. Apenas leitura. |
|externalPartnerTenantId|Guid| O identificador de locatário para o locatário do parceiro. Somente leitura. |
|id|String| O identificador exclusivo do recurso. Herdado de [directoryObject](/graph/api/resources/directoryobject?view=graph-rest-v1.0). Apenas leitura. |
|objectType|String| O tipo do objeto referenciado no locatário do parceiro. Somente leitura. |

## <a name="json-representation"></a>Representação JSON

Veja a seguir uma representação JSON do recurso.

<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.directoryObjectPartnerReference"
}-->

```json
{
  "description": "string ",
  "displayName": "string",
  "externalPartnerTenantId": "string (identifier)",
  "id": "string (identifier)",
  "objectType": "string"
}
```

## <a name="see-also"></a>Confira também

- [Obter objetos directory a partir de uma lista de ids](../api/directoryobject-getbyids.md)

<!-- uuid: fbec8cd7-cfe4-431d-87fc-d102cd2841a4
2018-12-06 02:01:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "directoryObjectPartnerReference resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->
