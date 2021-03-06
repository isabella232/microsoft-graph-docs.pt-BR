---
title: tipo de recurso governanceRoleAssignment
description: Representa a atribuição de um usuário ou grupo a uma função.
localization_priority: Normal
doc_type: resourcePageType
ms.prod: microsoft-identity-platform
author: shauliu
ms.openlocfilehash: fec241d2152fd4b2cea68159f3eb1c6154bacabe
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/18/2020
ms.locfileid: "48081683"
---
# <a name="governanceroleassignment-resource-type"></a>tipo de recurso governanceRoleAssignment

Namespace: Microsoft. Graph [!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Representa a atribuição de um usuário ou grupo a uma função.

O gerenciamento de identidade privilegiada (PIM) oferece suporte a dois tipos de atribuições:

1. Atribuição ativa – representa o acesso direto/ativado aos recursos.
2. Atribuição qualificada – representa um estágio intermediário de acesso privilegiado a recursos, entre sem acesso e acesso direto. Os administradores podem atribuir usuários/grupos com `eligible assignment` antecedência e sempre que o acesso for necessário, quando for necessário, `activation` `eligible assignment` para obter o acesso instantâneo ao recurso por várias horas. Após a ativação, um `active assignment` será criado para os membros de usuários/grupos para indicar o status ativado.

## <a name="methods"></a>Métodos

| Método          | Tipo de retorno |Descrição|
|:------------|:--------|:--------|
|[Get](../api/governanceroleassignment-get.md) |  [governanceRoleAssignment](../resources/governanceroleassignment.md) |Leia as propriedades e as relações de uma entidade de atribuição de função.|
|[List](../api/governanceroleassignment-list.md) | coleção [governanceRoleAssignment](../resources/governanceroleassignment.md)|Lista uma coleção de atribuições de função em um recurso. |
|[Export](../api/governanceroleassignment-export.md) | octeto-Stream |Baixe uma coleção de atribuições de função em um recurso e salve como um `.csv` arquivo.|

Nenhuma `POST` `PUT` `PATCH` `DELETE` operação é suportada no `roleAssignments` conjunto de entidades. Qualquer operação de criação, atualização e exclusão no `governanceRoleAssignment` é feita por `governanceRoleAssignmentRequest` .

## <a name="properties"></a>Propriedades
| Propriedade  | Tipo      |Descrição|
|:----------|:----------|:----------|
|id         |Cadeia de caracteres     |A ID da atribuição de função. Está no formato GUID.|
|resourceId |Cadeia de caracteres     |Obrigatório. A identificação do recurso ao qual a atribuição de função está associada. |
|roleDefinitionId|Cadeia de caracteres|Obrigatório. A ID da definição de função à qual a atribuição de função está associada. |
|SubjectID|Cadeia de caracteres       |Obrigatório. A ID da entidade à qual a atribuição de função está associada. |
|linkedEligibleRoleAssignmentId|Cadeia de caracteres|Se este é um `active assignment` e criado devido à ativação em um `eligible assignment` , ele representa o ID dele `eligible assignment` ; Caso contrário, o valor será `null` . |
|externalId   |Cadeia de caracteres     |A ID externa o recurso usado para identificar a atribuição de função no provedor.|
|startDateTime|DateTimeOffset|A hora de início da atribuição de função. O tipo Timestamp representa informações de data e hora usando o formato ISO 8601 e está sempre no horário UTC. Por exemplo, meia-noite em UTC no dia 1° de janeiro de 2014 teria esta aparência: `'2014-01-01T00:00:00Z'`|
|endDateTime|DateTimeOffset|Para uma atribuição de função não permanente, esse é o momento em que a atribuição de função será expirada. O tipo Timestamp representa informações de data e hora usando o formato ISO 8601 e está sempre no horário UTC. Por exemplo, meia-noite em UTC no dia 1° de janeiro de 2014 teria esta aparência: `'2014-01-01T00:00:00Z'`|
|assignmentstate|Cadeia de caracteres  |O estado da atribuição. O valor pode ser <ul><li> `Eligible` para atribuição qualificada</li><li> `Active` – Se ele for atribuído diretamente `Active` por administradores ou ativado em uma atribuição qualificada pelos usuários.</li></ul>|
|memberType|Cadeia de caracteres      |O tipo do membro. O valor pode ser: <ul><li>`Inherited` -a atribuição de função é herdada de um escopo de recurso pai</li><li>`Group`– a atribuição de função não é herdada, mas vem da Associação de uma atribuição de grupo</li><li>`User` – a atribuição de função não é herdada nem de uma atribuição de grupo.</li></ul>|


## <a name="relationships"></a>Relações
| Relação | Tipo   |Descrição|
|:---------------|:--------|:----------|
|recurso|[governanceResource](../resources/governanceresource.md)|Somente leitura. O recurso associado à atribuição de função. |
|roleDefinition|[governanceRoleDefinition](../resources/governanceroledefinition.md)|Somente leitura. A definição de função associada à atribuição de função. |
|assunto|[governanceSubject](../resources/governancesubject.md)|Somente leitura. O assunto associado à atribuição de função. |
|linkedEligibleRoleAssignment|[governanceRoleAssignment](../resources/governanceroleassignment.md)|Somente leitura. Se este é um `active assignment` e criado devido à ativação em um `eligible assignment` , ele representa o objeto desse `eligible assignment` ; Caso contrário, o valor será `null` . |

## <a name="json-representation"></a>Representação JSON

Veja a seguir uma representação JSON do recurso.


<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.governanceRoleAssignment"
}-->

```json
{
  "id": "String (identifier)",
  "resourceId": "String",
  "roleDefinitionId": "String",
  "subjectId": "String",
  "linkedEligibleRoleAssignmentId": "String",
  "externalId": "String",
  "startDateTime": "String (timestamp)",
  "endDateTime": "String (timestamp)",
  "assignmentState": "String",
  "memberType": "String",
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "governanceRoleAssignment",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->


