---
title: tipo de recurso permissionScope
description: Representa um escopo de permissão delegada do OAuth 2,0.
localization_priority: Normal
doc_type: resourcePageType
ms.prod: microsoft-identity-platform
author: davidmu1
ms.openlocfilehash: be8d9a7d08334bd716cfcbf565225add790b65e3
ms.sourcegitcommit: 62507617292d5ad8598e83a8a253c986d9bac787
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2019
ms.locfileid: "37939366"
---
# <a name="permissionscope-resource-type"></a>tipo de recurso permissionScope

Representa um escopo de permissão delegada do OAuth 2,0. Os escopos de permissão delegada do OAuth 2,0 especificado podem ser solicitados por aplicativos cliente (por meio da coleção **requiredResourceAccess** no objeto [Application](application.md) ) ao chamar um aplicativo de recurso. A propriedade **oauth2Permissions** <!-- of the [servicePrincipal](serviceprincipal.md) entity and --> a entidade do [aplicativo](application.md) é uma coleção de **permissionScope**.

## <a name="properties"></a>Propriedades

| Propriedade | Tipo | Descrição |
|:---------------|:--------|:----------|
|adminConsentDescription|Cadeia de caracteres| Texto de ajuda de permissão que aparece nas experiências de atribuição de aplicativo e consentimento de administrador. |
|adminConsentDisplayName|Cadeia de caracteres| Nome para exibição da permissão que aparece nas experiências de atribuição de aplicativo e consentimento de administrador. |
|id|Guid| Identificador de permissão de escopo exclusivo dentro da coleção oauth2Permissions. |
|isEnabled|Boolean| Ao criar ou atualizar uma permissão, essa propriedade deve ser definida como **true** (que é o padrão). Para excluir uma permissão, essa propriedade deve ser definida primeiro como **false**. Nesse ponto, em uma chamada subsequente, a permissão pode ser removida. |
|tenham|Cadeia de caracteres| Para uso interno. |
|type|Cadeia de caracteres| Especifica se essa permissão de escopo pode ser consentida por um usuário final ou se é uma permissão em todo o locatário que deve ser consentida pelo administrador da empresa. Os valores possíveis são *User* ou *admin*. |
|userConsentDescription|Cadeia de caracteres| Texto de ajuda de permissão que aparece na experiência de consentimento do usuário final. |
|userConsentDisplayName|Cadeia de caracteres| Nome para exibição da permissão que aparece na experiência de consentimento do usuário final. |
|value|Cadeia de caracteres| O valor da declaração do escopo que o aplicativo de recursos deve esperar no token de acesso do OAuth 2,0. |

## <a name="json-representation"></a>Representação JSON
Veja a seguir uma representação JSON do recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.permissionScope"
}-->

```json
{
  "adminConsentDescription": "String",
  "adminConsentDisplayName": "String",
  "id": "Guid",
  "isEnabled": true,
  "origin": "String",
  "type": "String",
  "userConsentDescription": "String",
  "userConsentDisplayName": "String",
  "value": "String"
}

```


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "permissionScope resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->