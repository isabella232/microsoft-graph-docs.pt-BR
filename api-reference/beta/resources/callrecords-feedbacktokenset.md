---
title: tipo de recurso feedbackTokenSet
description: O tipo feedbackTokenSet
localization_priority: Normal
author: williamlooney
ms.prod: cloud-communications
doc_type: resourcePageType
ms.openlocfilehash: 71a6d575cf09eda13c5f187b47516b4cbc2b185f
ms.sourcegitcommit: af4b2fc18449c33979cf6d75bd680f40602ba708
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "48601154"
---
# <a name="feedbacktokenset-resource-type"></a>tipo de recurso feedbackTokenSet

Namespace: microsoft.graph.callRecords

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Este é um _tipo aberto_ que representa o conjunto de tokens de comentários fornecidos pelo usuário deste ponto de extremidade para a sessão. Este é um conjunto de propriedades booleanas. Os nomes de propriedade não devem ser dependentes, já que eles podem ser alterados, dependendo de quais tokens são oferecidos para o usuário.

## <a name="properties"></a>Propriedades

Nomes de propriedades explícitas não serão documentados, pois os nomes de token de comentários podem mudar, portanto, este é um [tipo aberto](/aspnet/web-api/overview/odata-support-in-aspnet-web-api/odata-v4/use-open-types-in-odata-v4).

## <a name="json-representation"></a>Representação JSON

Veja a seguir uma representação JSON do recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.callRecords.feedbackTokenSet",
  "baseType": null
}-->

```json
{
  "DistortedSpeech": true,
  "ElectronicFeedback": false,
  "BackgroundNoise": true,
  "MuffledSpeech": true,
  "Echo": false
}
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "feedbackTokenSet resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->