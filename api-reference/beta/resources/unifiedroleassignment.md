---
title: tipo de recurso unifiedRoleAssignment
description: Uma atribuição de função é o vínculo entre uma definição de função e uma entidade de segurança em um escopo específico para o propósito de conceder acesso.
localization_priority: Normal
author: davidmu1
ms.prod: microsoft-identity-platform
doc_type: resourcePageType
ms.openlocfilehash: cfc0c00add243b98c852a00f0a4ab990c3ca5173
ms.sourcegitcommit: 567d0420243765b4088bc8029306a517f92926fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/16/2019
ms.locfileid: "36437787"
---
# <a name="unifiedroleassignment-resource-type"></a>tipo de recurso unifiedRoleAssignment

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Um unifiedRoleAssignment é usado para conceder acesso aos recursos. Ele representa uma definição de função atribuída a uma entidade de segurança (normalmente um usuário) em um determinado escopo.

## <a name="methods"></a>Métodos

| Método       | Tipo de retorno | Descrição |
|:-------------|:------------|:------------|
| [Obter unifiedRoleAssignment](../api/unifiedroleassignment-get.md) | [unifiedRoleAssignment](unifiedroleassignment.md) | Leia as propriedades e os relacionamentos do objeto unifiedRoleAssignment. |
| [Criar unifiedRoleAssignment](../api/rbacapplication-post-roleassignments.md) | [unifiedRoleAssignment](unifiedroleassignment.md) | Crie um novo unifiedRoleAssignment postando na coleção roleAssignment. |
| [Delete](../api/unifiedroleassignment-delete.md) | None | Exclua o objeto unifiedRoleAssignment. |

## <a name="properties"></a>Propriedades

| Propriedade     | Tipo        | Descrição |
|:-------------|:------------|:------------|
|id|String| O identificador exclusivo para o unifiedRoleAssignment. Chave, não anulável, somente leitura. |
|principalId|String| ObjectID da entidade de segurança para a qual a atribuição é concedida. |
|resourceScope|String| O escopo no qual o unifiedRoleAssignment se aplica. Isso é "/" para todo o serviço. |
|roleDefinitionId|String| O unifiedRoleDefinition para o qual a atribuição é. Somente leitura. |

## <a name="relationships"></a>Relações

Nenhum

## <a name="json-representation"></a>Representação JSON

Veja a seguir uma representação JSON do recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.unifiedRoleAssignment",
  "baseType": "",
  "keyProperty": "id"
}-->

```json
{
  "id": "String (identifier)",
  "principalId": "String",
  "resourceScope": "String",
  "roleDefinitionId": "String"
}
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "unifiedRoleAssignment resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->