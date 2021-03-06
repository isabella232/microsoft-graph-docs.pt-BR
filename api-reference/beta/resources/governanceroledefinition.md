---
title: tipo de recurso governanceRoleDefinition
description: Representa as definições de função. Para os recursos do Azure, ele pode representar as funções do Azure RBAC, como proprietário, leitor, colaborador, etc.
localization_priority: Normal
doc_type: resourcePageType
ms.prod: microsoft-identity-platform
author: shauliu
ms.openlocfilehash: b45a52734af115a872e7ff5f31c58ef5ed95b944
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/18/2020
ms.locfileid: "48081668"
---
# <a name="governanceroledefinition-resource-type"></a>tipo de recurso governanceRoleDefinition

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]


Representa as definições de função. Para os recursos do Azure, ele pode representar as funções do Azure RBAC, como proprietário, leitor, colaborador, etc.


## <a name="methods"></a>Métodos

| Método          | Tipo de retorno |Descrição|
|:---------------|:--------|:--------|
|[List](../api/governanceroledefinition-list.md) | coleção [governanceRoleDefinition](../resources/governanceroledefinition.md) |Lista uma coleção de definições de função em um recurso.|
|[Get](../api/governanceroledefinition-get.md) | [governanceRoleDefinition](../resources/governanceroledefinition.md) |Ler propriedades e relações de uma entidade de definição de função especificado por ID.|

Não `POST` , `PUT` , `PATCH` , `DELETE` tem suporte no `roleDefinitions` conjunto de entidades por enquanto.

## <a name="properties"></a>Propriedades
| Propriedade    | Tipo   | Descrição                                                           |
|:------------|:-------|:----------------------------------------------------------------------|
| id          | Cadeia de caracteres | A ID da definição de função.                                        |
| resourceId  | Cadeia de caracteres | Obrigatório. A ID do recurso associada à definição de função. |
| externalId  | Cadeia de caracteres | A ID externa da definição de função.                               |
| displayName | Cadeia de caracteres | O nome de exibição da definição de função.                              |
| templateId  | Cadeia de caracteres |                                                                       |

## <a name="relationships"></a>Relações
| Relação | Tipo   |Descrição|
|:---------------|:--------|:----------|
|recurso|[governanceResource](../resources/governanceresource.md)|Somente leitura. O recurso associado para a definição de função.|
|roleSetting|[governanceRoleSetting](../resources/governancerolesetting.md)|A configuração de função associada para a definição de função.|

## <a name="json-representation"></a>Representação JSON

Veja a seguir uma representação JSON do recurso.

<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.governanceRoleDefinition"
}-->

```json
{
  "id": "String (identifier)",
  "resourceId": "String",
  "externalId": "String",
  "displayName": "String",
  "templateId":"String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "governanceRoleDefinition",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->


