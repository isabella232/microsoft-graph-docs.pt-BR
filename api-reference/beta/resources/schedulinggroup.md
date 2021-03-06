---
title: tipo de recurso schedulingGroup
description: Um agrupamento lógico de membros do cronograma (geralmente pela função).
author: nkramer
localization_priority: Priority
ms.prod: microsoft-teams
doc_type: resourcePageType
ms.openlocfilehash: db86b22f61b7293683a775460cb3678af7ca4f5a
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/18/2020
ms.locfileid: "47985801"
---
# <a name="schedulinggroup-resource-type"></a>tipo de recurso schedulingGroup

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Um agrupamento lógico de usuários em um [cronograma](schedule.md) (geralmente pela função). 

## <a name="methods"></a>Métodos

| Método       | Tipo de retorno  |Descrição|
|:---------------|:--------|:----------|
|[Criar schedulingGroup](../api/schedule-post-schedulinggroups.md) | [schedulingGroup](schedulinggroup.md) | Criar uma página `schedulingGroup`.|
|[Lista schedulingGroups](../api/schedule-list-schedulinggroups.md) | [schedulingGroup](schedulinggroup.md) conjunto | Obter uma lista dos `schedulingGroups` em um cronograma.|
|[Obter schedulingGroup](../api/schedulinggroup-get.md) | [schedulingGroup](schedulinggroup.md) | Obter um `schedulingGroup` por ID.|
|[Subtituir schedulingGroup](../api/schedulinggroup-put.md) | [schedulingGroup](schedulinggroup.md) | Substituir um `schedulingGroup`.|
|[Excluir schedulingGroup](../api/schedulinggroup-delete.md) | Nenhum | Marcar `schedulingGroup` como inativa.|

## <a name="properties"></a>Propriedades
|Nome          |Tipo           |Descrição                                                                                 |
|--------------|---------------|--------------------------------------------------------------------------------------------|
| id            | `string`      |A ID da tarefa `schedulingGroup`.|
| Nome para exibição   | `string`      | O nome de exibição do grupo `schedulingGroup`. Obrigatório. |
| isActive          |`bool`      | Indica se o `schedulingGroup` pode ser usada na criação de novas entidades ou atualizar as existentes. Obrigatório. |
| userIds       | `collection(string)`    |  A lista de IDs é membro de usuários da `schedulingGroup`. Obrigatório. |
| createdDateTime       |`DateTimeOffset`        |O carimbo de hora em que isso `schedulingGroup` foi criado pela primeira vez. O tipo Timestamp representa informações de data e hora usando o formato ISO 8601 e está sempre no horário UTC. Por exemplo, meia-noite em UTC no dia 1º de janeiro de 2014 teria esta aparência: '2014-01-01T00:00:00Z'. |
| lastModifiedDateTime      |`DateTimeOffset`        |O carimbo de hora em que isso `schedulingGroup` foi criado pela última vez. O tipo Timestamp representa informações de data e hora usando o formato ISO 8601 e está sempre no horário UTC. Por exemplo, meia-noite em UTC no dia 1º de janeiro de 2014 teria esta aparência: '2014-01-01T00:00:00Z'. |
| lastModifiedBy        | [identitySet](identityset.md) |A identidade da última atualização `schedulingGroup`.|

## <a name="json-representation"></a>Representação JSON

Veja a seguir uma representação JSON do recurso.

<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.schedulingGroup",
  "baseType": "microsoft.graph.changeTrackedEntity"
}-->

```json
{
  "id": "string (identifier)",
  "createdDateTime": "String (timestamp)",
  "lastModifiedDateTime": "String (timestamp)",
  "displayName": "String",
  "isActive": true,
  "userIds": ["String (identifier)"],
  "lastModifiedBy":{"@odata.type":"microsoft.graph.identitySet"}
}
```


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "schedulingGroup resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->


