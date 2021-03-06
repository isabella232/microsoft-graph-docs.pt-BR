---
title: tipo de recurso onPremisesProvisioningError
description: Representa erros de sincronização de diretório para o grupo de usuários e recursos de contato durante a sincronização de diretórios locais com o Azure Active Directory.
localization_priority: Normal
author: japere
ms.prod: microsoft-identity-platform
doc_type: resourcePageType
ms.openlocfilehash: 719bb525fad934bb92f44fb427d1214bf288ec46
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/18/2020
ms.locfileid: "48059086"
---
# <a name="onpremisesprovisioningerror-resource-type"></a>tipo de recurso onPremisesProvisioningError

Namespace: microsoft.graph

Representa erros de sincronização de diretório para os recursos de [usuário](user.md), [grupo](group.md) e [orgContact](orgcontact.md) ao sincronizar diretórios locais com o Azure Active Directory.

## <a name="properties"></a>Propriedades

| Propriedade | Tipo | Descrição |
|:---------------|:--------|:----------|
|category|String| Categoria do erro de provisionamento. Observação: no momento, há apenas um valor possível. Valor possível: *PropertyConflict* -indica que um valor de propriedade não é exclusivo. Outros objetos contêm o mesmo valor para a propriedade. |
|occurredDateTime|DateTimeOffset| A data e a hora em que o erro ocorreu. |
|propertyCausingError|String| Nome da propriedade de diretório que está causando o erro. Valores possíveis atuais: *userPrincipalName* ou *ProxyAddress* |
|value|Cadeia de caracteres| Valor da propriedade causando o erro. |

## <a name="json-representation"></a>Representação JSON
Veja a seguir uma representação JSON do recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.onPremisesProvisioningError"
}-->

```json
{
  "category": "String",
  "occurredDateTime": "String (timestamp)",
  "propertyCausingError": "String",
  "value": "String"
}

```


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "onPremisesProvisioningError resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

