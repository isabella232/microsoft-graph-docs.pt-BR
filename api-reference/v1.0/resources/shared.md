---
author: JeremyKelley
ms.author: JeremyKelley
ms.date: 09/10/2017
title: Compartilhados
localization_priority: Normal
description: O recurso Shared indica que um DriveItem foi compartilhado com outras pessoas.
ms.prod: ''
doc_type: resourcePageType
ms.openlocfilehash: 9058b1e3f5f8dd77c22ee253746c7eba8c1df7c1
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/18/2020
ms.locfileid: "48009181"
---
# <a name="shared-resource-type"></a>Tipo de recurso Shared

Namespace: microsoft.graph

O recurso **Shared** indica que um DriveItem foi compartilhado com outras pessoas. O recurso inclui informações sobre como o item é compartilhado.

Se um [**Driveitem**](driveitem.md) tem uma faceta **shared** não nula, o item foi compartilhada.

## <a name="json-representation"></a>Representação JSON

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.shared",
  "optionalProperties": [ "sharedBy", "sharedDateTime" ]
}-->

```json
{
  "owner": { "@odata.type": "microsoft.graph.identitySet" },
  "scope": "anonymous | organization | users",
  "sharedBy": { "@odata.type": "microsoft.graph.identitySet" },
  "sharedDateTime": "datetime"
}
```

## <a name="properties"></a>Propriedades

| Propriedade       | Tipo                          | Descrição
| :------------- |:------------------------------|:----------------------------
| owner          | [IdentitySet](identityset.md) | A identidade do proprietário do item compartilhado. Somente leitura.
| escopo          | String                        | Indica o escopo de como o item é compartilhado: `anonymous`, `organization` ou `users`. Somente leitura.
| sharedBy       | [identitySet](identityset.md) | A identidade do usuário que compartilhou o item. Somente leitura.
| sharedDateTime | DateTimeOffset                | A data e a hora UTC que o item foi compartilhado. Somente leitura.

## <a name="scope-options"></a>Opções de escopo

| Valor          | Descrição                                                                           |
|:---------------|:--------------------------------------------------------------------------------------|
| `anonymous`    | O item é compartilhado usando-se um link que funciona para qualquer pessoa que tem o link.               |
| `organization` | O item é compartilhado usando-se um link que funciona para qualquer pessoa na organização do proprietário. |
| `users`        | O item é compartilhado apenas com usuários específicos.                                          |

## <a name="remarks"></a>Comentários

Para saber mais sobre as facetas de um **driveItem**, confira [**driveItem**](driveitem.md).

<!-- {
  "type": "#page.annotation",
  "description": "The shared facet provides info about shared items.",
  "keywords": "shared,share,item,facet,onedrive",
  "section": "documentation",
  "suppressions": [
    "Warning: /api-reference/v1.0/resources/shared.md:
      Found potential enums in resource example that weren't defined in a table:(anonymous,organization,users) are in resource, but () are in table"
  ],
  "tocPath": "Facets/Shared"
} -->

