---
title: tipo de recurso educationRubric
description: Uma amostra rubric de gradação que pode ser anexada a uma atribuição
localization_priority: Normal
author: dipakboyed
ms.prod: education
doc_type: resourcePageType
ms.openlocfilehash: 154e153166c45a0eb671ab554d1b8ed337fb9830
ms.sourcegitcommit: 7ceec757fd82ef3fd80aa3089ef46d3807aa3aa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2020
ms.locfileid: "48406069"
---
# <a name="educationrubric-resource-type"></a>tipo de recurso educationRubric

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Um amostra rubric de gradação que pode ser anexado a uma atribuição. Um amostra rubric é associado a um **educationUser** (professor) e anexado a um ou mais recursos do **educationAssignment** . 

Consulte [Education amostra rubric Overview](/graph/education-rubric-overview) para obter mais informações.

## <a name="methods"></a>Métodos

| Método       | Tipo de retorno | Descrição |
|:-------------|:------------|:------------|
| [Criar educationRubric](../api/educationuser-post-rubrics.md) | [educationRubric](educationrubric.md) | Criar um novo objeto educationRubric. |
| [Obter educationRubric](../api/educationrubric-get.md) | [educationRubric](educationrubric.md) | Leia as propriedades e os relacionamentos do objeto educationRubric. |
| [Atualizar educationRubric](../api/educationrubric-update.md) | [educationRubric](educationrubric.md) | Atualize o objeto educationRubric. |
| [Excluir educationRubric](../api/educationrubric-delete.md) | Nenhum | Exclua o objeto educationRubric. |

## <a name="properties"></a>Propriedades

| Propriedade     | Tipo        | Descrição |
|:-------------|:------------|:------------|
|createdBy|[identitySet](identityset.md)|O usuário que criou este recurso.|
|createdDateTime|DateTimeOffset|O tipo Timestamp representa informações de data e hora usando o formato ISO 8601 e está sempre no horário UTC. Por exemplo, meia-noite em UTC no dia 1º de janeiro de 2014 teria esta aparência: `'2014-01-01T00:00:00Z'`|
|description|[itemBody](itembody.md)|A descrição desse amostra rubric.|
|displayName|Cadeia de caracteres|O nome deste amostra rubric.|
|notas|[educationAssignmentGradeType](educationassignmentgradetype.md)|O tipo de gradação desse amostra rubric-NULL para um amostra rubric sem pontos, ou [educationAssignmentPointsGradeType](educationassignmentpointsgradetype.md) para um ponto amostra rubric.|
|lastModifiedBy|[identitySet](identityset.md)|O último usuário a modificar o recurso.|
|lastModifiedDateTime|DateTimeOffset|Momento no momento em que o recurso foi modificado pela última vez.  O tipo Timestamp representa informações de data e hora usando o formato ISO 8601 e está sempre no horário UTC. Por exemplo, meia-noite em UTC no dia 1º de janeiro de 2014 teria esta aparência: `'2014-01-01T00:00:00Z'`|
|alcançar|coleção [rubricLevel](rubriclevel.md)|A coleção de níveis que compõem este amostra rubric.|
|qualidades|coleção [rubricQuality](rubricquality.md)|O conjunto de qualidades que compõem este amostra rubric.|

## <a name="relationships"></a>Relações

Nenhum

## <a name="json-representation"></a>Representação JSON

Veja a seguir uma representação JSON do recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.educationRubric",
  "baseType": "",
  "keyProperty": "id"
}-->

```json
{
  "createdBy": {"@odata.type": "microsoft.graph.identitySet"},
  "createdDateTime": "String (timestamp)",
  "description": {"@odata.type": "microsoft.graph.itemBody"},
  "displayName": "String",
  "grading": {"@odata.type": "microsoft.graph.educationAssignmentGradeType"},
  "lastModifiedBy": {"@odata.type": "microsoft.graph.identitySet"},
  "lastModifiedDateTime": "String (timestamp)",
  "levels": [{"@odata.type": "microsoft.graph.rubricLevel"}],
  "qualities": [{"@odata.type": "microsoft.graph.rubricQuality"}]
}
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "educationRubric resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->