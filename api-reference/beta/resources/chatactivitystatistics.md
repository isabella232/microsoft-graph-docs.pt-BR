---
title: tipo de recurso chatActivityStatistics
description: Representa informações sobre atividades de chat para usuários.
localization_priority: Normal
author: madehmer
ms.prod: insights
doc_type: resourcePageType
ms.openlocfilehash: a380ef18435ca971da4f3163fc1268ec7f28e565
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/18/2020
ms.locfileid: "48064343"
---
# <a name="chatactivitystatistics-resource-type"></a>tipo de recurso chatActivityStatistics

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Representa dados sobre o tempo gasto pelo usuário em atividades de chat no Microsoft Teams ou no Skype for Business. Isso é baseado no [activityStatistics](../resources/activitystatistics.md).

## <a name="properties"></a>Propriedades

| Propriedade     | Tipo        | Descrição |
|:-------------|:------------|:------------|
|atividade|analyticsActivityType| Atividade de chat para a qual as estatísticas são retornadas.|
|duration|Duração|Total de horas gasto em chats. O valor é representado no formato ISO 8601 para durações.|
|endDate|Data|Data de término da atividade de chat. O valor é representado no formato ISO 8601 para datas do calendário. Por exemplo, o valor da propriedade poderia ser "2019-07-04" que segue o formato AAAA-MM-DD.|
|id|Cadeia de caracteres| ID somente leitura da atividade de chat.|
|startDate|Data|Data de início da atividade de chat. O valor é representado no formato ISO 8601 para datas do calendário. Por exemplo, o valor da propriedade poderia ser "2019-07-03" que segue o formato AAAA-MM-DD.|
|timeZoneUsed|Cadeia de caracteres|O fuso horário que o usuário define no calendário do Outlook é usado para a computação. Por exemplo, o valor da propriedade poderia ser "hora padrão do Pacífico".|
|afterHours|Duração|Tempo gasto em chats fora do horário de trabalho, que se baseia na configuração de calendário do Microsoft Outlook do usuário para horário de trabalho. O valor é representado no formato ISO 8601 para durações. |

## <a name="relationships"></a>Relações

Nenhum

## <a name="json-representation"></a>Representação JSON

Veja a seguir uma representação JSON do recurso.

<!-- {
  "blockType": "resource",
  "baseType": "microsoft.graph.activityStatistics",
  "keyProperty": "id", 
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.chatActivityStatistics"
}-->

```json
{
  "activity": "string",
  "duration": "String (ISO 8601 duration)",
  "endDate": "String (ISO 8601)",
  "id": "String (identifier)",
  "startDate": "String (ISO 8601)",
  "timeZoneUsed": "String",
  "afterHours": "String (ISO 8601 duration)"
}

```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "chatActivityStatistics resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->



