---
title: tipo de recurso conditionalAccessPolicy
description: Representa uma política de acesso condicional do Azure Active Directory. As políticas de acesso condicional são regras personalizadas que definem um cenário do Access.
localization_priority: Normal
author: videor
ms.prod: microsoft-identity-platform
doc_type: resourcePageType
ms.openlocfilehash: 70ba87f751c7dc61a71578b845df9978b7148f60
ms.sourcegitcommit: 7ceec757fd82ef3fd80aa3089ef46d3807aa3aa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2020
ms.locfileid: "48402974"
---
# <a name="conditionalaccesspolicy-resource-type"></a>tipo de recurso conditionalAccessPolicy

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Representa uma política de acesso condicional do Azure Active Directory. As políticas de acesso condicional são regras personalizadas que definem um cenário do Access. Para obter mais informações, consulte a [documentação de acesso condicional](/azure/active-directory/conditional-access/).

## <a name="methods"></a>Métodos

| Método       | Tipo de retorno | Descrição |
|:-------------|:------------|:------------|
| [Listar conditionalAccessPolicies](../api/conditionalaccessroot-list-policies.md) | [conditionalAccessPolicy](conditionalaccesspolicy.md) conjunto | Obter todos os objetos conditionalAccessPolicies na organização. |
| [Criar conditionalAccessPolicy](../api/conditionalaccessroot-post-policies.md) | [conditionalAccessPolicy](conditionalaccesspolicy.md) | Criar um novo objeto conditionalAccessPolicy. |
| [Obter conditionalAccessPolicy](../api/conditionalaccesspolicy-get.md) | [conditionalAccessPolicy](conditionalaccesspolicy.md) | Ler propriedades e relações de um objeto conditionalAccessPolicy. |
| [Atualizar conditionalAccessPolicy](../api/conditionalaccesspolicy-update.md) | [conditionalAccessPolicy](conditionalaccesspolicy.md) | Atualizar um objeto conditionalAccessPolicy. |
| [Excluir conditionalAccessPolicy](../api/conditionalaccesspolicy-delete.md) | Nenhum | Excluir um objeto conditionalAccessPolicy. |

## <a name="properties"></a>Propriedades

| Propriedade     | Tipo        | Descrição |
|:-------------|:------------|:------------|
|conditions|[conditionalAccessConditionSet](conditionalaccessconditionset.md)| Especifica as regras que devem ser atendidas para que a política seja aplicada. Obrigatório. |
|createdDateTime|DateTimeOffset| O tipo Timestamp representa informações de data e hora usando o formato ISO 8601 e está sempre no horário UTC. Por exemplo, meia-noite em UTC no dia 1º de janeiro de 2014 teria esta aparência: `'2014-01-01T00:00:00Z'`. ReadOnly. |
|description|Cadeia de caracteres| Não usado. |
|displayName|Cadeia de caracteres| Especifica um nome de exibição para o objeto conditionalAccessPolicy. |
|grantControls|[conditionalAccessGrantControls](conditionalaccessgrantcontrols.md)| Especifica os controles de concessão que devem ser atendidos para passar a política. |
|id|Cadeia de caracteres| Especifica o identificador de um objeto conditionalAccessPolicy. Somente leitura.|
|modifiedDateTime| DateTimeOffset|O tipo Timestamp representa informações de data e hora usando o formato ISO 8601 e está sempre no horário UTC. Por exemplo, meia-noite em UTC no dia 1º de janeiro de 2014 teria esta aparência: `'2014-01-01T00:00:00Z'`. ReadOnly. |
|sessionControls|[conditionalAccessSessionControls](conditionalaccesssessioncontrols.md)| Especifica os controles de sessão que são aplicados após a entrada. |
|estado|string| Especifica o estado do objeto conditionalAccessPolicy. Os valores possíveis são: `enabled`, `disabled`, `enabledForReportingButNotEnforced`. Obrigatório. |

## <a name="relationships"></a>Relações

Nenhum

## <a name="json-representation"></a>Representação JSON

Veja a seguir uma representação JSON do recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "displayName",
    "description",
    "sessionControls",
    "grantControls"
  ],
  "@odata.type": "microsoft.graph.conditionalAccessPolicy",
  "baseType": "",
  "keyProperty": "id"
}-->

```json
{
  "conditions": {"@odata.type": "microsoft.graph.conditionalAccessConditionSet"},
  "createdDateTime": "String (timestamp)",
  "description": "String",
  "displayName": "String",
  "grantControls": {"@odata.type": "microsoft.graph.conditionalAccessGrantControls"},
  "id": "String (identifier)",
  "modifiedDateTime": "String (timestamp)",
  "sessionControls": {"@odata.type": "microsoft.graph.conditionalAccessSessionControls"},
  "state": "string"
}
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "conditionalAccessPolicy resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->