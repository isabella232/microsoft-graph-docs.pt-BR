---
title: Tipo de recurso appRoleAssignment
description: Utilizado para registro quando um usuário, grupo ou entidade de serviço é atribuído a uma função de aplicativo na entidade de serviço de um aplicativo. Você pode criar, ler e excluir as atribuições de função.
localization_priority: Priority
doc_type: resourcePageType
ms.prod: microsoft-identity-platform
author: psignoret
ms.openlocfilehash: c23c0a9d4e3f41ca21b285eb7f5484678c3d8b66
ms.sourcegitcommit: 7ceec757fd82ef3fd80aa3089ef46d3807aa3aa2
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2020
ms.locfileid: "48405621"
---
# <a name="approleassignment-resource-type"></a>Tipo de recurso appRoleAssignment

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Utilizado para registro quando um usuário, grupo ou entidade de serviço recebe uma função de aplicativo para um aplicativo.

Uma atribuição de função de aplicativo é uma relação entre a entidade de segurança atribuída (um usuário, um grupo ou uma entidade de serviço), um aplicativo de recursos (a entidade de serviço do aplicativo) e uma função de aplicativo definida no aplicativo de recurso.

Quando a [função de aplicativo](approle.md) que foi atribuída a uma entidade tem uma propriedade de **valor** não vazio, isso será incluído nas **funções** de declaração de tokens em que o assunto é a entidade de segurança atribuída (por exemplo, respostas SAML, tokens de identificação, tokens de acesso identificando um usuário conectado ou um token de acesso identificando uma entidade de serviço). Os aplicativos e as APIs usam essas declarações como parte da lógica de autorização.

É possível atribuir uma função de aplicativo diretamente a um usuário. Se uma função de aplicativo for atribuída a um grupo, os membros diretos do grupo também serão considerados atribuídos à função de aplicativo. Quando um usuário recebe uma função de aplicativo para um aplicativo, o bloco do aplicativo é exibido no portal [MyApps](/azure/active-directory/user-help/my-apps-portal-end-user-access) e no[inicializador de aplicativos do Microsoft 365](https://support.office.com/article/meet-the-office-365-app-launcher-79f12104-6fed-442f-96a0-eb089a3f476a).

Uma atribuição de função de aplicativo onde a entidade de segurança atribuída é uma entidade de serviço é uma permissão [somente para aplicativo](/azure/active-directory/develop/v2-permissions-and-consent#permission-types). Quando um usuário ou administrador consentir a uma permissão somente para aplicativo, será criada uma atribuição de função de aplicativo onde a entidade de segurança atribuída é a entidade de serviço do aplicativo cliente e o recurso é a entidade de serviço da API de destino.

## <a name="properties"></a>Propriedades

| Propriedade | Tipo | Descrição |
|:---------------|:--------|:----------|
| id | Cadeia de caracteres | Um identificador exclusivo para a chave **appRoleAssignment**. Não anulável. Somente leitura. |
| creationTimestamp | DateTimeOffset | A hora em que a atribuição de função do aplicativo foi criada. O tipo timestamp representa informações de data e hora usando o formato ISO 8601 e está sempre no horário UTC. Por exemplo, meia-noite em UTC no dia 1º de janeiro de 2014 teria esta aparência: `'2014-01-01T00:00:00Z'`. Somente leitura. O não tem suporte para `$filter`. |
| principalId | Guid | O identificador exclusivo (**id**) para o [usuário](user.md), [grupo](group.md) ou da [entidade](serviceprincipal.md) a qual o acesso está sendo concedido. Obrigatório durante a criação. O não tem suporte para `$filter`. |
| principalType | Cadeia de caracteres | O tipo da entidade de segurança atribuída. Pode ser “Usuário”, “Grupo” ou “ServicePrincipal”. Somente leitura. O não tem suporte para `$filter`. |
| principalDisplayName | Cadeia de caracteres |O nome de exibição do usuário, grupo ou entidade de serviço que recebeu a atribuição de função do aplicativo. Somente leitura. Suporte para `$filter` (`eq` e `startswith`). |
| resourceId | Guid |Identificador exclusivo (**id**) para o recurso [(entidade de serviço)](serviceprincipal.md) para o qual a atribuição foi feita. Obrigatório durante a criação. Suporte para `$filter` (`eq` somente). |
| resourceDisplayName | Cadeia de caracteres | O nome de exibição da entidade de serviço da função do aplicativo para o qual a atribuição foi feita. O não tem suporte para `$filter`. |
| appRoleId | Guid | O identificador (**id**) da [função do aplicativo](approle.md) que está atribuída à entidade de segurança. Essa função de aplicativo deve ser exposta na propriedade **appRoles** na entidade de serviço do aplicativo de recurso (**ResourceId**). Se o aplicativo de recurso não tiver declarado todas as funções do aplicativo, uma ID de função de aplicativo padrão de `00000000-0000-0000-0000-000000000000` poderá ser especificada para sinalizar que a entidade de segurança está atribuída ao aplicativo de recursos sem nenhuma função específica do aplicativo. Obrigatório durante a criação. O não tem suporte para `$filter`. |

## <a name="json-representation"></a>Representação JSON

Veja a seguir uma representação JSON do recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.appRoleAssignment"
}-->

```json
{
  "id": "string",
  "creationTimestamp": "String (timestamp)",
  "principalDisplayName": "string",
  "principalId": "guid",
  "principalType": "string",
  "resourceDisplayName": "string",
  "resourceId": "guid",
  "appRoleId": "guid"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "appRoleAssignment resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->