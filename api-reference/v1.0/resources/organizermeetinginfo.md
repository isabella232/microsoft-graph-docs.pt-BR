---
title: tipo de recurso organizerMeetingInfo
description: 'Contém detalhes sobre o organizador da reunião. '
author: ananmishr
localization_priority: Normal
ms.prod: cloud-communications
doc_type: resourcePageType
ms.openlocfilehash: d3b1f37e6ac5f33d6d59988054d5abfedf5e68e7
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/18/2020
ms.locfileid: "48066282"
---
# <a name="organizermeetinginfo-resource-type"></a>tipo de recurso organizerMeetingInfo

Namespace: microsoft.graph

Contém detalhes sobre o organizador da reunião. 

Para ingressar em uma reunião existente, você deve fornecer uma combinação dos tipos de recurso organizerMeetingInfo e [chatInfo](./chatinfo.md) ou o tipo de recurso [tokenMeetingInfo](./tokenmeetinginfo.md) sozinho.

## <a name="properties"></a>Propriedades

| Propriedade                     | Tipo                          | Descrição                                     |
| :--------------------------- | :---------------------------- | :-----------------------------------------------|
| organizer                    | [identitySet](identityset.md) | A identidade do Azure Active Directory do organizador.  |

## <a name="json-representation"></a>Representação JSON

Veja a seguir uma representação JSON do recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.organizerMeetingInfo"
}-->
```json
{
  "organizer": { "@odata.type": "#microsoft.graph.identitySet" }
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "organizerMeetingInfo resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->

