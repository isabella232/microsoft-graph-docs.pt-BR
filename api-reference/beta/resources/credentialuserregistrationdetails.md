---
title: tipo de recurso credentialUserRegistrationDetails
description: Representa os detalhes do uso da redefinição de senha de autoatendimento e da MFA (autenticação multifator) para todos os usuários registrados.
localization_priority: Normal
author: khotz
ms.prod: reports
doc_type: resourcePageType
ms.openlocfilehash: 7194f1b849decddcca5d77bf0ebb9bbbd5974125
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/18/2020
ms.locfileid: "48050014"
---
# <a name="credentialuserregistrationdetails-resource-type"></a>tipo de recurso credentialUserRegistrationDetails

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Representa os detalhes do uso da redefinição de senha de autoatendimento e da MFA (autenticação multifator) para todos os usuários registrados. Os detalhes incluem informações do usuário, status do registro e o método de autenticação usado.

## <a name="methods"></a>Métodos

| Método       | Tipo de retorno | Descrição |
|:-------------|:------------|:------------|
| [Listar credentialUserRegistrationDetails](../api/reportroot-list-credentialuserregistrationdetails.md) | coleção credentialUserRegistrationDetails | Obter uma lista de objetos [credentialUserRegistrationDetails](../resources/credentialuserregistrationdetails.md) para um determinado locatário.
 |

## <a name="properties"></a>Propriedades

| Propriedade     | Tipo        | Descrição |
|:-------------|:------------|:------------|
| authMethods | coleção registrationAuthMethod | Representa o método de autenticação que o usuário registrou. Os valores possíveis são: `email` , `mobilePhone` , `officePhone` , `securityQuestion` (usado somente para redefinição de senha de autoatendimento),, `appNotification` `appCode` e `alternateMobilePhone` (com suporte apenas no registro). |
| id | Cadeia de caracteres | O identificador exclusivo da atividade. Somente leitura.|
| iscapable | Booliano | Indica se o usuário está pronto para executar a redefinição de senha de autoatendimento ou a MFA. |
| isEnabled | Boolean | Indiciates se o usuário está habilitado para executar redefinição de senha de autoatendimento. |
| isMfaRegistered | Booliano | Indiciates se o usuário está registrado para MFA. |
| IsRegistered | Booliano | Indica se o usuário registrou todos os métodos de autenticação para redefinição de senha de autoatendimento. |
| userDisplayName | Cadeia de caracteres | Fornece o nome de usuário do usuário correspondente. |
| userPrincipalName | Cadeia de caracteres | Fornece o nome principal de usuário do usuário correspondente. |

## <a name="relationships"></a>Relações

Nenhum

## <a name="json-representation"></a>Representação JSON

Veja a seguir uma representação JSON do recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.credentialUserRegistrationDetails",
  "baseType": "",
  "keyProperty": "id"
}-->

```json
{
  "id" : "String",
  "userPrincipalName":"String",
  "userDisplayName": "String",
  "authMethods": ["string"],
  "isRegistered" : false,
  "isEnabled" : true,
  "isCapable" : false,
  "isMfaRegistered" : true
}
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "credentialUserRegistrationDetails resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->


