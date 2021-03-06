---
title: tipo de recurso usersecuritystate
description: Contém informações monitoradoras sobre a conta de usuário.
author: krbain
localization_priority: Normal
ms.prod: microsoft-identity-platform
doc_type: resourcePageType
ms.openlocfilehash: ae085791cb60aa6d5071332ead86033861a6305a
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/18/2020
ms.locfileid: "48015369"
---
# <a name="usersecuritystate-resource-type"></a>tipo de recurso usersecuritystate

Namespace: microsoft.graph

Contém informações monitoradoras sobre a conta de usuário.

## <a name="properties"></a>Propriedades

| Propriedade   | Tipo |Descrição|
|:---------------|:--------|:----------|
|aadUserId|String|GUID (identificador de objeto do usuário) do AAD – representa a entidade de usuário física/de várias contas.|
|accountName|String|Nome da conta da conta de usuário (sem o domínio do Active Directory ou domínio DNS)-(também chamado `mailNickName` ).|
|domainName|Cadeia de caracteres|Domínio NetBIOS/Active Directory da conta de usuário (ou seja, formato de domínio \ conta).|
|emailRole|emailRole|Para alertas relacionados a email-a função de email da conta de usuário. Os valores possíveis são: `unknown`, `sender`, `recipient`.|
|isVpn|Boolean|Indica se o usuário fez logon por meio de uma VPN.|
|logonDateTime|DateTimeOffset|Hora em que o logon ocorreu. O tipo Timestamp representa informações de data e hora usando o formato ISO 8601 e está sempre no horário UTC. Por exemplo, meia-noite em UTC no dia 1º de janeiro de 2014 teria esta aparência: `'2014-01-01T00:00:00Z'`.|
|LogonId|String|ID de entrada do usuário.|
|logonIp|String|Endereço IP para o qual a solicitação de entrada originou.|
|logonLocation|String|Local (por mapeamento de endereço IP) associado a um evento de entrada do usuário por este usuário.|
|logonType|logonType|Método de logon do usuário. Os possíveis valores são: `unknown`, `interactive`, `remoteInteractive`, `network`, `batch`, `service`.|
|onPremisesSecurityIdentifier|String|O identificador de segurança (SID) do usuário do Active Directory (local).|
|riskScore|String|A pontuação de risco calculado/gerado pelo provedor da conta de usuário. O intervalo de valor recomendado de 0-1, que é igual a uma porcentagem.|
|useraccounttype|userAccountSecurityType|Tipo de conta de usuário (Associação de grupo), por definição do Windows. Os valores possíveis são: `unknown`, `standard`, `power`, `administrator`.|
|userPrincipalName|String|Nome de entrada do usuário-formato da Internet: (nome da conta de usuário) @ (nome de domínio DNS da conta de usuário).|

## <a name="json-representation"></a>Representação JSON

Veja a seguir uma representação JSON do recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.userSecurityState"
}-->

```json
{
  "aadUserId": "String",
  "accountName": "String",
  "domainName": "String",
  "emailRole": "@odata.type: microsoft.graph.emailRole",
  "isVpn": true,
  "logonDateTime": "String (timestamp)",
  "logonId": "String",
  "logonIp": "String",
  "logonLocation": "String",
  "logonType": "@odata.type: microsoft.graph.logonType",
  "onPremisesSecurityIdentifier": "String",
  "riskScore": "String",
  "userAccountType": "@odata.type: microsoft.graph.userAccountSecurityType",
  "userPrincipalName": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "userSecurityState resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

