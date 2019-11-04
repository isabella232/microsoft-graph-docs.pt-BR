---
title: tipo de recurso appRole
description: Representa uma função de aplicativo que pode ser solicitada por um aplicativo cliente que esteja ligando para outro aplicativo.
localization_priority: Normal
doc_type: resourcePageType
ms.prod: microsoft-identity-platform
author: davidmu1
ms.openlocfilehash: f98cb4d1c32256dccf5e2748116cdd7fc1869f68
ms.sourcegitcommit: 62507617292d5ad8598e83a8a253c986d9bac787
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2019
ms.locfileid: "37937389"
---
# <a name="approle-resource-type"></a>tipo de recurso appRole

Representa uma função de aplicativo que pode ser solicitada por um aplicativo cliente que esteja chamando outro aplicativo ou que possa ser usada para atribuir um aplicativo a usuários ou grupos em uma função de aplicativo especificada. A propriedade **appRoles** <!-- of the [servicePrincipal](serviceprincipal.md) entity and --> a entidade do [aplicativo](application.md) é uma coleção de **appRole**.

## <a name="properties"></a>Propriedades
| Propriedade     | Tipo   |Descrição|
|:---------------|:--------|:----------|
|allowedMemberTypes|String collection|Especifica se essa definição de função de aplicativo pode ser atribuída a usuários e grupos por meio da configuração de "usuário" ou a outros aplicativos (que estão acessando esse aplicativo em cenários de serviço de daemon) definindo como "aplicativo" ou ambos.|
|description|String|Texto de ajuda de permissão que aparece nas experiências de consentimento e atribuição de aplicativo de administração.|
|displayName|Cadeia de caracteres|Nome para exibição da permissão que aparece nas experiências de atribuição de aplicativo e consentimento de administrador.|
|id|Guid|Identificador de função exclusivo dentro da coleção **appRoles** . Ao criar uma nova função de aplicativo, um novo identificador GUID deve ser fornecido. |
|isEnabled|Boolean|Ao criar ou atualizar uma função de aplicativo, isso deve ser definido como **true** (que é o padrão). Para excluir uma função, é necessário primeiro defini-la como **false**.  Nesse ponto, em uma chamada subsequente, essa função pode ser removida.|
|tenham|String| Somente leitura. Especifica se a função de aplicativo é definida no objeto Application <!-- or on the ServicePrincipal object -->. _Não_ deve ser incluído em solicitações POST ou patch. |
|value|Cadeia de caracteres|Especifica o valor que será incluído na `roles` declaração em tokens de autenticação e de acesso. Não deve exceder 120 caracteres de comprimento. Caracteres `:` `!` `#` `$` permitidos são `%` `&` `'` `(` `)` `*` `+` `,` `-` `.` `/` `:` `;` <code>&lt;</code> `=` <code>&gt;</code> `?` `A-Z` como os caracteres nos intervalos `a-z`e. `0-9` `^` `@` `[` `]` `+` `_` <code>&#96;</code> `{` <code>&#124;</code> `}` `~` Qualquer outro caractere, incluindo o caractere de espaço, não é permitido.  |

## <a name="json-representation"></a>Representação JSON

Veja a seguir uma representação JSON do recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.appRole"
}-->

```json
{
  "allowedMemberTypes": ["string"],
  "description": "string",
  "displayName": "string",
  "id": "guid",
  "isEnabled": true,
  "origin": "string",
  "value": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "appRole resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->