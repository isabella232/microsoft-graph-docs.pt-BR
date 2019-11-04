---
title: tipo de recurso fallbackPolicyProperties
description: 'Permite que a política de fallback seja especificada para notificações brutas de alta prioridade somente nos pontos de extremidade do iOS, com propriedades adicionais para especificar o tempo de espera de fallback (atraso) e o conteúdo de notificação Visual correspondente. '
localization_priority: Normal
author: merzink
ms.prod: notifications
doc_type: resourcePageType
ms.openlocfilehash: a3ce59a23b5aec6dd43b370c3b67e9439b11937e
ms.sourcegitcommit: 62507617292d5ad8598e83a8a253c986d9bac787
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2019
ms.locfileid: "37938959"
---
# <a name="fallbackpolicyproperties-resource-type"></a>tipo de recurso fallbackPolicyProperties

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Permite que a política de fallback seja especificada para notificações brutas de alta prioridade somente nos pontos de extremidade do iOS, com propriedades adicionais para especificar o tempo de espera de fallback (atraso) e o conteúdo de notificação Visual correspondente. 

## <a name="properties"></a>Propriedades

| Propriedade     | Tipo        | Descrição |
|:-------------|:------------|:------------|
| platformTypes | String collection | Especifica as plataformas que um desenvolvedor deseja habilitar para o fallback de notificação de torradeira de leitura para leitura visual. No momento, se **fallbackPolicy** for especificado, **targetPolicy. platformTypes** deve `iOS` incluir e opcionalmente outras plataformas. Além disso, o **fallbackPolicy. endpointFallback. platformTypes** é necessário e a única plataforma suportada atualmente `iOS`. |
| fallbackDelayInSeconds | Int32 | Esse atraso representa a quantidade de tempo que passará (em segundos) antes que uma notificação de notificação direta seja enviada como um fallback para cada usuário de assinatura de dispositivo iOS que não buscará a notificação bruta. O valor deve estar entre 60 e 600. |
| visualContent | [visualproperties](visualproperties.md)|O conteúdo visual de uma notificação de usuário de retorno de fallback e bruto para Visual no iOS. |
 


## <a name="json-representation"></a>Representação JSON

Veja a seguir uma representação JSON do recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.fallbackpolicyProperties",
  "baseType": null
}-->

```json
{
  "platformTypes": ["String"],
  "fallbackDelayInSeconds": 60,
  "visualContent": {"@odata.type": "microsoft.graph.visualProperties"}
}
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "fallbackpolicyProperties resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->