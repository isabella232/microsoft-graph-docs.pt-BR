---
title: tipo de recurso keycredential
description: Contém uma credencial de chave associada a um aplicativo ou a uma entidade de serviço. A propriedade **Keycredentials** do aplicativo e das entidades do servicePrincipalName é uma coleção de **keycredential**.
localization_priority: Normal
doc_type: resourcePageType
ms.prod: microsoft-identity-platform
author: sureshja
ms.openlocfilehash: 6c005a44827640ed7a61e61f07837a98021d9a9c
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/18/2020
ms.locfileid: "48078336"
---
# <a name="keycredential-resource-type"></a>tipo de recurso keycredential

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Contém uma credencial de chave associada a um aplicativo ou a uma entidade de serviço. A propriedade **Keycredentials** do [aplicativo](application.md) e das entidades do [servicePrincipalName](serviceprincipal.md) é uma coleção de **keycredential**.

## <a name="properties"></a>Propriedades
| Propriedade     | Tipo   |Descrição|
|:---------------|:--------|:----------|
|customKeyIdentifier|Binária| Identificador de chave personalizada |
| displayName | Cadeia de caracteres | Nome amigável para a chave. Opcional. |
|endDateTime|DateTimeOffset|A data e a hora em que a credencial expira. O tipo TIMESTAMP representa informações de data e hora usando o formato ISO 8601 e está sempre no horário UTC. Por exemplo, meia-noite em UTC no dia 1° de janeiro de 2014 teria esta aparência: `'2014-01-01T00:00:00Z'`|
|keyId|Guid|O identificador exclusivo (GUID) da chave.|
|startDateTime|DateTimeOffset|A data e a hora em que a credencial se torna válida. O tipo TIMESTAMP representa informações de data e hora usando o formato ISO 8601 e está sempre no horário UTC. Por exemplo, meia-noite em UTC no dia 1° de janeiro de 2014 teria esta aparência: `'2014-01-01T00:00:00Z'`|
|tipo|Cadeia de caracteres|O tipo de credencial de chave; por exemplo, "simétrico".|
|ocorrência|Cadeia de caracteres|Uma cadeia de caracteres que descreve a finalidade para a qual a chave pode ser usada; por exemplo, "Verify".|
|chave|Binário| Valor para a credencial de chave. Deve ser um valor codificado de base 64. |

## <a name="json-representation"></a>Representação JSON

Veja a seguir uma representação JSON do recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.keyCredential"
}-->

```json
{
  "customKeyIdentifier": "binary",
  "displayName": "String",
  "endDateTime": "String (timestamp)",
  "keyId": "guid",
  "startDateTime": "String (timestamp)",
  "type": "string",
  "usage": "string",
  "key": "binary"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "keyCredential resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->


