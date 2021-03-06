---
title: tipo de recurso openShiftChangeRequest
description: Representa um tipo de solicitação de mudança para declarar um turno aberto em um cronograma.
localization_priority: Normal
author: akumar39
ms.prod: microsoft-teams
doc_type: resourcePageType
ms.openlocfilehash: 26dccf0d0e79e2f0427f07035ee31e5480c52b95
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/18/2020
ms.locfileid: "47998555"
---
# <a name="openshiftchangerequest-resource-type"></a>tipo de recurso openShiftChangeRequest

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Representa um tipo de solicitação de mudança para declarar um [openshift](../resources/openshift.md) em um [cronograma](../resources/schedule.md).

## <a name="methods"></a>Methods

| Método       | Tipo de retorno | Descrição |
|:-------------|:------------|:------------|
| [Criar](../api/openshiftchangerequest-post.md) | [openshiftchangerequest](openshiftchangerequest.md) | Criar uma instância de um objeto openshiftchangerequest. |
| [List](../api/openshiftchangerequest-list.md) | Coleção de [openshiftchangerequest](openshiftchangerequest.md) | Listar as propriedades e os relacionamentos dos objetos **openShiftChangeRequest** em uma equipe. |
| [Get](../api/openshiftchangerequest-get.md) | [openShiftChangeRequest](openshiftchangerequest.md) | Leia as propriedades e os relacionamentos de um objeto **openShiftChangeRequest** . |
|[Aprovar](../api/openshiftchangerequest-approve.md)|Nenhum|Aprovar uma solicitação de alteração de turno aberta.|
|[Aceito](../api/openshiftchangerequest-decline.md)|Nenhum| Recusar uma solicitação de alteração de turno aberto.|

## <a name="properties"></a>Propriedades

| Propriedade     | Tipo        | Descrição |
|:-------------|:------------|:------------|
|openShiftId|String| ID para o turno aberto.|

## <a name="relationships"></a>Relações

Nenhum

## <a name="json-representation"></a>Representação JSON

Veja a seguir uma representação JSON do recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.openShiftChangeRequest",
  "baseType": ""
}-->

```json
{
  "openShiftId": "String"
}
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "openShiftChangeRequest resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->


