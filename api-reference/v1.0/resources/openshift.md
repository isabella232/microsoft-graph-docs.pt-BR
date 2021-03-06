---
title: tipo de recurso openShift
description: Representa um turno aberto não atribuído em um cronograma.
localization_priority: Normal
author: akumar39
ms.prod: microsoft-teams
doc_type: resourcePageType
ms.openlocfilehash: 4a1a616cee4f61a93f8b3db379a0e5f39afc5f22
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/18/2020
ms.locfileid: "48003028"
---
# <a name="openshift-resource-type"></a>tipo de recurso openShift

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Representa um turno não atribuído e aberto em um [cronograma](../resources/schedule.md).

## <a name="methods"></a>Methods

| Método       | Tipo de retorno | Descrição |
|:-------------|:------------|:------------|
| [List](../api/openshift-list.md) | Coleção de [openShift](openshift.md) | Listar as propriedades e os relacionamentos dos objetos **openShift** em uma equipe.|
| [Create](../api/openshift-post.md) | [openShift](openshift.md) | Criar uma instância de um objeto **openShift** . |
| [Get](../api/openshift-get.md) | [openShift](openshift.md) | Leia as propriedades e os relacionamentos de um objeto **openShift** . |
| [Atualização](../api/openshift-update.md) | [openShift](openshift.md) | Atualize um objeto **openShift** . |
| [Delete](../api/openshift-delete.md) | Nenhum | Excluir um objeto **openShift** . |

## <a name="properties"></a>Propriedades

| Propriedade     | Tipo        | Descrição |
|:-------------|:------------|:------------|
|draftOpenShift|[openShiftItem](openshiftitem.md)|Um turno aberto não publicado.|
|schedulingGroupId|String|ID do grupo de agendamento ao qual o turno aberto pertence.|
|sharedOpenShift|[openShiftItem](openshiftitem.md)|Um turno aberto publicado.|

## <a name="relationships"></a>Relações

Nenhum

## <a name="json-representation"></a>Representação JSON

Veja a seguir uma representação JSON do recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.openShift",
  "baseType": ""
}-->

```json
{
  "draftOpenShift": {"@odata.type": "microsoft.graph.openShiftItem"},
  "schedulingGroupId": "String",
  "sharedOpenShift": {"@odata.type": "microsoft.graph.openShiftItem"}
}
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "openShift resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

