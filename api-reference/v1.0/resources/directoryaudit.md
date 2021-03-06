---
title: Tipo de recurso directoryObject
description: Representa os itens de auditoria de diretório e sua coleção.
author: SarahBar
localization_priority: Normal
ms.prod: microsoft-identity-platform
doc_type: resourcePageType
ms.openlocfilehash: 07941fd2878495eaedcbb67ee667f82f6d7bbdfb
ms.sourcegitcommit: eb536655ffd8d49ae258664f35c50a8263238400
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/18/2020
ms.locfileid: "49230762"
---
# <a name="directoryaudit-resource-type"></a>Tipo de recurso directoryObject

Namespace: microsoft.graph

Representa os itens de auditoria de diretório e sua coleção.

## <a name="methods"></a>Métodos

| Método           | Tipo de retorno    |Descrição|
|:---------------|:--------|:----------|
|[Lista directoryAudits](../api/directoryaudit-list.md) | [directoryAudit](directoryaudit.md) |Liste os itens de auditoria de diretório no conjunto de suas propriedades.|
|[Obter directoryAudit](../api/directoryaudit-get.md) | [directoryAudit](directoryaudit.md) |Obter um item de auditoria do diretório específico e suas propriedades.|

## <a name="properties"></a>Propriedades

| Propriedade            | Tipo                                                | Descrição                                                                                                                                                                                                                                                                        |
|:--------------------|:----------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| activityDateTime    | DateTimeOffset                                      | Indica a data e hora que a atividade foi executada. O tipo de Timestamp é sempre UTC. Por exemplo, meia-noite em UTC no dia 1º de janeiro de 2014 teria esta aparência: `'2014-01-01T00:00:00Z'`                                                                                          |
| activityDisplayName | Cadeia de caracteres                                              | Indica o nome da atividade ou o nome da operação (exemplos: "criar usuário" e "Adicionar membro ao grupo"). Para obter uma lista completa, confira [lista de atividades do Azure ad](/azure/active-directory/active-directory-reporting-activity-audit-logs#azure-ad-audit-activity-list). |
| additionalDetails   | Coleção [KeyValue](keyvalue.md)                  | Indica detalhes adicionais sobre a atividade.                                                                                                                                                                                                                                      |
| category            | Cadeia de caracteres                                              | Indica qual categoria de recurso direcionada pela atividade. (Por exemplo: gerenciamento de usuário, grupo gerenciamento etc..)                                                                                                                                                          |
| correlationId       | GUID                                                | Indica uma ID exclusiva que ajuda correlacionar atividades que englobam vários serviços. Pode ser usado para os logs de serviços de rastreamento.                                                                                                                                                |
| id                  | Cadeia de caracteres                                              | Indica que a ID exclusiva para a atividade. Este é um GUID.                                                                                                                                                                                                                          |
| initiatedBy         | [auditActivityInitiator](auditactivityinitiator.md) | Indica que informações sobre o usuário ou o aplicativo iniciou a atividade.                                                                                                                                                                                                                |
| loggedByService     | Cadeia de caracteres                                              | Indica informação em que o serviço iniciou a atividade (por exemplo: gerenciamento de senha de autoatendimento, principais diretório, B2C, os usuários convidados, Microsoft Identity Manager, Privileged Identity Management.                                                                      |
| resultado              | cadeia de caracteres                                              | Indica o resultado da atividade. Os valores possíveis são: `success`, `failure`, `timeout`, `unknownFutureValue`.                                                                                                                                                                   |
| resultReason        | Cadeia de caracteres                                              | Descreve a causa dos resultados de "falha" ou "tempo limite".                                                                                                                                                                                                                                 |
| targetResources     | [targetResource](targetresource.md) conjunto      | Indica informação que o recurso foi alterado devido a atividade. Tipo de recurso de destino pode ser usuário, dispositivo, diretório, aplicativos, função, grupo, política ou outros.                                                                                                                   |

## <a name="relationships"></a>Relações

Nenhum

## <a name="json-representation"></a>Representação JSON

Veja a seguir uma representação JSON do recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.directoryAudit"
}-->

```json
{
  "activityDateTime": "String (timestamp)",
  "activityDisplayName": "String",
  "additionalDetails": [{"@odata.type": "microsoft.graph.keyValue"}],
  "category": "String",
  "correlationId": "Guid",
  "id": "String (identifier)",
  "initiatedBy": {"@odata.type": "microsoft.graph.auditActivityInitiator"},
  "loggedByService": "String",
  "result": "string",
  "resultReason": "String",
  "targetResources": [{"@odata.type": "microsoft.graph.targetResource"}]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "directoryAudit resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
