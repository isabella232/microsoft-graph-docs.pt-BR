---
title: tipo de recurso removeProtectionAction
description: Representa uma ação para remover a proteção do arquivo ou informações.
localization_priority: Normal
author: tommoser
ms.prod: microsoft-identity-platform
doc_type: resourcePageType
ms.openlocfilehash: bf4ad367038367d3572f0451bfa7d3eb0a25368d
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/18/2020
ms.locfileid: "48073394"
---
# <a name="removeprotectionaction-resource-type"></a>tipo de recurso removeProtectionAction

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Representa uma ação para remover a proteção do arquivo ou informações. As APIs [evaluateApplication](../api/informationprotectionlabel-evaluateapplication.md), [evaluateClassificationResults](../api/informationprotectionlabel-evaluateclassificationresults.md)ou [evaluateRemoval](../api/informationprotectionlabel-evaluateremoval.md) podem retornar o **removeProtectionAction** se a proteção for removida como resultado da atualização ou remoção do rótulo. A ação instrui o aplicativo de consumo a remover o elemento de interface do usuário específico que contém o cabeçalho de conteúdo aplicável anteriormente. A proteção deve ser removida por uma biblioteca de cliente, como o Microsoft Information Protection SDK, somente se o usuário de chamada tiver direitos suficientes para remover a proteção.

## <a name="properties"></a>Propriedades

Nenhum

## <a name="json-representation"></a>Representação JSON

Veja a seguir uma representação JSON do recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.removeProtectionAction",
  "baseType": "microsoft.graph.informationProtectionAction"
}-->

```json
{
  
}
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "removeProtectionAction resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

