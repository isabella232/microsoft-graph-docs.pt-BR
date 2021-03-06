---
title: tipo de recurso educationSubmission
description: Os envios são propriedade de uma atribuição. Um envio representa os recursos que um indivíduo (ou grupo) liga para uma atribuição e a grade/comentários que é retornado.
author: dipakboyed
localization_priority: Normal
ms.prod: education
doc_type: resourcePageType
ms.openlocfilehash: 3a917a6d74b47b3e42d2457c5bf747abbf237cf4
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/18/2020
ms.locfileid: "47979575"
---
# <a name="educationsubmission-resource-type"></a>tipo de recurso educationSubmission

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Os envios são propriedade de uma atribuição. Um envio representa os recursos que um indivíduo (ou grupo) liga para uma atribuição e os resultados (como notas ou comentários) associados ao envio.
Os envios são criados automaticamente quando uma atribuição é publicada. O envio possui duas listas de recursos. Os recursos representam a área de trabalho usuários/grupos enquanto os recursos enviados representam os recursos que foram ativamente ativados pelos alunos.  

>**Observação:** O status é somente leitura e o objeto é movido através do fluxo de trabalho via ações. 

## <a name="methods"></a>Methods

| Método           | Tipo de retorno    |Descrição|
|:---------------|:--------|:----------|
|[Obter educationSubmission](../api/educationsubmission-get.md) | [educationSubmission](educationsubmission.md) |Ler propriedades e relações de um objeto **educationSubmission** .|
|[Listar recursos](../api/educationsubmission-list-resources.md) |coleção [educationSubmissionResource](educationsubmissionresource.md)| Obtenha uma coleção de objetos **educationSubmissionResource** .|
|[Listar submittedResources](../api/educationsubmission-list-submittedresources.md) |coleção [educationSubmissionResource](educationsubmissionresource.md)| Obtenha uma coleção de objetos **educationSubmissionResource** .|
|[Resultados de lista](../api/educationsubmission-list-outcomes.md) |coleção [educationOutcome](educationoutcome.md)| Obtenha uma coleção de objetos **educationOutcome** .|
|[Enter](../api/educationsubmission-return.md)|[educationSubmission](educationsubmission.md)|Um professor usa Return para indicar que os notas/comentários podem ser mostrados para o aluno.|
|[Enviar](../api/educationsubmission-submit.md)|[educationSubmission](educationsubmission.md)|Um aluno usa Submit para ativar a atribuição. Isso copiará os recursos na pasta **submittedResources** para a gradação e atualizará o status.|
|[Não enviar](../api/educationsubmission-unsubmit.md)|[educationSubmission](educationsubmission.md)|Um aluno usa o não enviar para mover o estado do envio de enviado de volta para o trabalho. Isso copiará os recursos na pasta **workingResources** para a gradação e atualizará o status.|

## <a name="properties"></a>Propriedades
| Propriedade     | Tipo   |Descrição|
|:---------------|:--------|:----------|
|destinatário|[educationSubmissionRecipient](educationsubmissionrecipient.md)|A quem esse envio é atribuído.|
|releasedBy|[identitySet](identityset.md)|Usuário que moveu o status desse envio para liberado.|
|releasedDateTime|DateTimeOffset|Momento no momento em que o envio foi lançado. O tipo Timestamp representa informações de data e hora usando o formato ISO 8601 e está sempre no horário UTC. Por exemplo, meia-noite em UTC no dia 1° de janeiro de 2014 teria esta aparência: `'2014-01-01T00:00:00Z'`|
|returnedBy|[identitySet](identityset.md)|Usuário que moveu o status desse envio para o retornado.|
|returnedDateTime|DateTimeOffset|Momento no momento em que o envio foi retornado. O tipo Timestamp representa informações de data e hora usando o formato ISO 8601 e está sempre no horário UTC. Por exemplo, meia-noite em UTC no dia 1° de janeiro de 2014 teria esta aparência: `'2014-01-01T00:00:00Z'`|
|resourcesFolderUrl|String|Pasta onde todos os recursos de arquivo para esse envio precisam ser armazenados.|
|status|cadeia de caracteres| Somente Leitura. Os valores possíveis são: `working`, `submitted`, `released`, `returned`.|
|submittedBy|[identitySet](identityset.md)|Usuário que moveu o recurso para o estado enviado.|
|submittedDateTime|DateTimeOffset|Momento no momento em que o envio foi movido para o estado enviado. O tipo Timestamp representa informações de data e hora usando o formato ISO 8601 e está sempre no horário UTC. Por exemplo, meia-noite em UTC no dia 1° de janeiro de 2014 teria esta aparência: `'2014-01-01T00:00:00Z'`|
|unsubmittedBy|[identitySet](identityset.md)|Usuário que moveu o recurso de enviado para o estado de trabalho.|
|unsubmittedDateTime|DateTimeOffset|Momento no momento em que o envio foi movido de enviado para o estado de trabalho. O tipo Timestamp representa informações de data e hora usando o formato ISO 8601 e está sempre no horário UTC. Por exemplo, meia-noite em UTC no dia 1° de janeiro de 2014 teria esta aparência: `'2014-01-01T00:00:00Z'`|

## <a name="relationships"></a>Relações
| Relação | Tipo   |Descrição|
|:---------------|:--------|:----------|
|recursos|coleção [educationSubmissionResource](educationsubmissionresource.md)| Anulável.|
|submittedResources|coleção [educationSubmissionResource](educationsubmissionresource.md)| Somente leitura. Anulável.|
|resultados|coleção [educationOutcome](educationOutcome.md) . Contém notas, comentários e/ou rubrics informações que o professor atribui a esse envio|Leitura-gravação. Anulável.|

## <a name="json-representation"></a>Representação JSON

Veja a seguir uma representação JSON do recurso.

<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.educationSubmission"
}-->

```json
{
    "id":"String (identifier)",
    "recipient":{"@odata.type":"microsoft.graph.educationSubmissionRecipient"},
    "returnedBy":{"@odata.type":"microsoft.graph.identitySet"},
    "returnedDateTime":"String (timestamp)",
    "resourcesFolderUrl":"String",
    "status":"string",
    "submittedBy":{"@odata.type":"microsoft.graph.identitySet"},
    "submittedDateTime":"String (timestamp)",
    "unsubmittedBy":{"@odata.type":"microsoft.graph.identitySet"},
    "unsubmittedDateTime":"String (timestamp)",
    "releasedBy":{"@odata.type":"microsoft.graph.identitySet"},
    "releasedDateTime":"String (timestamp)"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "educationSubmission resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->


