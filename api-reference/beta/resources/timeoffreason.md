---
title: tipo de recurso timeOffReason
description: Uma razão válida para ser demorada no cronograma.
author: nkramer
localization_priority: Normal
ms.prod: microsoft-teams
doc_type: resourcePageType
ms.openlocfilehash: 3a08ad02b03b3b39385f6f351e727d8b5ed54af1
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/18/2020
ms.locfileid: "48075478"
---
# <a name="timeoffreason-resource-type"></a>tipo de recurso timeOffReason

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Uma razão válida para uma instância do [timeOff](timeoff.md) em um [cronograma](schedule.md).

## <a name="methods"></a>Métodos

| Método       | Tipo de retorno  |Descrição|
|:---------------|:--------|:----------|
|[Criar](../api/schedule-post-timeoffreasons.md) | [timeOffReason](timeoffreason.md) | Criar um novo **timeOffReason**.|
|[List](../api/schedule-list-timeoffreasons.md) | coleção [timeOffReason](timeoffreason.md) | Obtenha a lista de **timeOffReason** em um cronograma.|
|[Get](../api/timeoffreason-get.md) | [timeOffReason](timeoffreason.md) | Obtenha um **timeOffReason** por ID.|
|[Replace](../api/timeoffreason-put.md) | [timeOffReason](timeoffreason.md) | Substitua um **timeOffReason**.|
|[Delete](../api/timeoffreason-delete.md) | Nenhum | Marcar um **timeOffReason** como inativo.|

## <a name="properties"></a>Propriedades
|Nome          |Tipo           |Descrição                                                                                 |
|--------------|---------------|--------------------------------------------------------------------------------------------|
| id            |`string`      |A ID da tarefa `timeOffReason`.|
| Nome para exibição               | `string`                  | O nome do `timeOffReason` . Obrigatório. |
| icontype | `timeOffReasonIconType`   | Tipos de ícone suportados: nenhum; automóvel dos com plano firstAid; Doutor Não funciona; medição juryDuty; Globe copo telefone Weather abrangência piggyBank; cachorro torta trafficCone; pessoal ensolarado. Obrigatório. |
| isActive          |`Boolean`      | Indica se o `timeOffReason` pode ser usada na criação de novas entidades ou atualizar as existentes. Obrigatório. |
| createdDateTime       |`DateTimeOffset`        |O carimbo de data/hora em que `timeOffReason` foi criado pela primeira vez. O tipo Timestamp representa informações de data e hora usando o formato ISO 8601 e está sempre no horário UTC. Por exemplo, meia-noite em UTC no dia 1º de janeiro de 2014 teria esta aparência: '2014-01-01T00:00:00Z'. |
| lastModifiedDateTime      |`DateTimeOffset`         |O carimbo de data/hora em que `timeOffReason` foi atualizado pela última vez. O tipo Timestamp representa informações de data e hora usando o formato ISO 8601 e está sempre no horário UTC. Por exemplo, meia-noite em UTC no dia 1º de janeiro de 2014 teria esta aparência: '2014-01-01T00:00:00Z'. |
| lastModifiedBy        | [identitySet](identityset.md)        |A identidade da última atualização `timeOffReason`.|

## <a name="json-representation"></a>Representação JSON

Veja a seguir uma representação JSON do recurso.

<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.timeOffReason",
  "baseType":"microsoft.graph.changeTrackedEntity"
}-->

```json
{
  "id": "String",
  "createdDateTime": "String (timestamp)",
  "lastModifiedDateTime": "String (timestamp)",
  "displayName": "String",
  "iconType": "String",
  "isActive": true,
  "lastModifiedBy": { "@odata.type":"microsoft.graph.identitySet"}
}
```


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "timeOffReason resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->


