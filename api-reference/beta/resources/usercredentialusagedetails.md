---
title: tipo de recurso userCredentialUsageDetails
description: Representa o uso de redefinição de senha de autoatendimento para um determinado locatário.
localization_priority: Normal
author: khotz
ms.prod: reports
doc_type: resourcePageType
ms.openlocfilehash: 3e00dfe9efccfa9e79d685b80d18524c0991e42e
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/18/2020
ms.locfileid: "48057897"
---
# <a name="usercredentialusagedetails-resource-type"></a>tipo de recurso userCredentialUsageDetails

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Representa o uso de redefinição de senha de autoatendimento para um determinado locatário. Os detalhes incluem informações do usuário, status da redefinição e o motivo da falha.

## <a name="methods"></a>Métodos

| Método       | Tipo de retorno | Descrição |
|:-------------|:------------|:------------|
| [Listar userCredentialUsageDetails](../api/reportroot-list-usercredentialusagedetails.md) | userCredentialUsageDetails | Ler propriedades e relações de um objeto userCredentialUsageDetails. |

## <a name="properties"></a>Propriedades

| Propriedade     | Tipo        | Descrição |
|:-------------|:------------|:------------|
| authMethod | cadeia de caracteres | Representa o método de autenticação usado pelo usuário. Os valores possíveis são: `email` , `mobileSMS` ,, `mobileCall` `officePhone` , `securityQuestion` (usado somente para redefinição de senha de autoatendimento), e (somente para o `appNotification` `appCode` `alternateMobileCall` registro). |
| eventDateTime | DateTimeOffset | O tipo Timestamp representa informações de data e hora usando o formato ISO 8601 e está sempre no horário UTC. Por exemplo, meia-noite em UTC no dia 1º de janeiro de 2014 teria esta aparência: `'2014-01-01T00:00:00Z'`. |
| failureReason | Cadeia de caracteres | Fornece o motivo da falha para o fluxo de trabalho de redefinição ou registro correspondente. |
| apresentam | cadeia de caracteres | Os valores possíveis são: `registration` e `reset` . |
| id | String | Somente leitura. O identificador exclusivo da atividade. Somente leitura.|
| IsSuccess | Booliano | Indica êxito ou falha do fluxo de trabalho. |
| userDisplayName | Cadeia de caracteres | Nome de usuário do usuário que está executando o fluxo de trabalho de redefinição ou registro. |
| userPrincipalName | Cadeia de caracteres | Nome principal do usuário que está executando o fluxo de trabalho de redefinição ou registro. |

## <a name="relationships"></a>Relações

Nenhum

## <a name="json-representation"></a>Representação JSON

Veja a seguir uma representação JSON do recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.userCredentialUsageDetails",
  "baseType": "",
  "keyProperty": "id"
}-->

```json
{
  "id" : "String",
  "feature":"string",
  "userPrincipalName":"String",
  "userDisplayName": "String",
  "isSuccess" : true,
  "authMethod": "string",
  "failureReason": "String",
  "eventDateTime" : "DateTimeOffset"
}
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "userCredentialUsageDetails resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

