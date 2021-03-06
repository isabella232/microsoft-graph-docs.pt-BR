---
title: tipo de recurso threatAssessmentRequest
description: Um tipo de recurso abstrato usado para representar um item de solicitação de avaliação de ameaça.
localization_priority: Normal
author: hafen-ms
ms.prod: microsoft-identity-platform
doc_type: resourcePageType
ms.openlocfilehash: df3f501ad281bcfced2e476b90e95b663fedef58
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/18/2020
ms.locfileid: "48090890"
---
# <a name="threatassessmentrequest-resource-type"></a>tipo de recurso threatAssessmentRequest

Um tipo de recurso abstrato usado para representar um item de solicitação de avaliação de ameaça.

Uma solicitação de avaliação de ameaça pode ser um dos seguintes tipos:

* Email (recurso[mailAssessmentRequest](mailAssessmentRequest.md) )
* Arquivo de email (recurso[emailFileAssessmentRequest](emailFileAssessmentRequest.md) )
* Arquivo (recurso[fileAssessmentRequest](fileAssessmentRequest.md) )
* URL (recurso[urlAssessmentRequest](urlAssessmentRequest.md) )

## <a name="methods"></a>Métodos

| Método       | Tipo de retorno | Descrição |
|:-------------|:------------|:------------|
| [List threatAssessmentRequest](../api/informationprotection-list-threatassessmentrequests.md) | coleção [threatAssessmentRequest](threatassessmentrequest.md) | Listar todas as solicitações de avaliação de ameaça sob locatário. |
| [Create threatAssessmentRequest](../api/informationprotection-post-threatassessmentrequests.md) | [threatAssessmentRequest](threatassessmentrequest.md) | Crie uma nova solicitação de avaliação de ameaça postando um tipo de recurso derivado: [mailAssessmentRequest](../resources/mailAssessmentRequest.md), [emailFileAssessmentRequest](../resources/emailFileAssessmentRequest.md), [fileAssessmentRequest](../resources/fileAssessmentRequest.md), [urlAssessmentRequest](../resources/urlAssessmentRequest.md). |
| [Get threatAssessmentRequest](../api/threatassessmentrequest-get.md) | [threatAssessmentRequest](threatassessmentrequest.md) | Recupere as propriedades e os relacionamentos de um recurso **threatAssessmentRequest** especificado. |

## <a name="properties"></a>Propriedades

| Propriedade     | Tipo        | Descrição |
| :-------------|:------------|:------------|
|Ferramentas para desenvolvedores|[threatCategory](enums.md#threatcategory-values)|A categoria da ameaça. Os valores possíveis são: `spam`, `phishing`, `malware`.|
|contentType|[threatAssessmentContentType](enums.md#threatassessmentcontenttype-values)|O tipo de conteúdo de avaliação de ameaça. Os valores possíveis são: `mail`, `url`, `file`.|
|createdBy|[identitySet](identityset.md)|O criador da solicitação de avaliação de ameaças.|
|createdDateTime|DateTimeOffset|O tipo Timestamp representa informações de data e hora usando o formato ISO 8601 e está sempre no horário UTC. Por exemplo, meia-noite em UTC no dia 1º de janeiro de 2014 teria esta aparência: `'2014-01-01T00:00:00Z'`.|
|expectedAssessment|[threatExpectedAssessment](enums.md#threatexpectedassessment-values)|A avaliação esperada do emissor. Os valores possíveis são: `block` e `unblock`.|
|id|Cadeia de caracteres|A ID da solicitação de avaliação da ameaça é um identificador global exclusivo (GUID).|
|objectrequest|[threatAssessmentRequestSource](enums.md#threatassessmentrequestsource-values)|A origem da solicitação de avaliação da ameaça. Os valores possíveis são: `user` e `administrator`.|
|status|[threatAssessmentStatus](enums.md#threatassessmentstatus-values)|O status do processo de avaliação. Os valores possíveis são: `pending`, `completed`.|

## <a name="relationships"></a>Relações

| Relação | Tipo        | Descrição |
|:-------------|:------------|:------------|
|resultados|coleção [threatAssessmentResult](threatassessmentresult.md)|Uma coleção de resultados de avaliação de ameaças. Somente leitura. Por padrão, um `GET /threatAssessmentRequests/{id}` não retorna essa propriedade, a menos que você a aplique `$expand` .|

## <a name="json-representation"></a>Representação JSON

Veja a seguir uma representação JSON do recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.threatAssessmentRequest",
  "baseType": "",
  "keyProperty": "id"
}-->

```json
{
  "category": "String",
  "contentType": "String",
  "createdBy": {"@odata.type": "microsoft.graph.identitySet"},
  "createdDateTime": "String (timestamp)",
  "expectedAssessment": "String",
  "id": "String (identifier)",
  "requestSource": "String",
  "status": "String"
}
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "threatAssessmentRequest resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

