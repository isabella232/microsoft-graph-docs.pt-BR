---
title: tipo de recurso hostSecurityState
description: Contém informações de estado sobre o host (incluindo dispositivos, computadores e assim por diante).
localization_priority: Normal
author: preetikr
ms.prod: ''
doc_type: resourcePageType
ms.openlocfilehash: 2d8543512162398f38f9ddb74cf72f57171c58f8
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/18/2020
ms.locfileid: "48062880"
---
# <a name="hostsecuritystate-resource-type"></a>tipo de recurso hostSecurityState

Namespace: microsoft.graph

Contém informações de estado sobre o host (incluindo dispositivos, computadores e assim por diante).

## <a name="properties"></a>Propriedades

| Propriedade   | Tipo|Descrição|
|:---------------|:--------|:----------|
|FQDN|String|FQDN do host (nome de domínio totalmente qualificado) (por exemplo, `machine.company.com` ).|
|isAzureAadJoined|Boolean|True se o host estiver associado ao domínio nos serviços de domínio do Azure Active Directory.|
|isAzureAadRegistered|Boolean|True se o host registrado no registro de dispositivo do Azure Active Directory (dispositivos BYOD-ou seja, não é totalmente gerenciado pela empresa).|
|isHybridAzureDomainJoined|Boolean|True se o host é membro de um domínio do Active Directory local.|
|NetBiosName|String|O nome do host local, sem o nome de domínio DNS.|
|Opera|String|Sistema operacional host. (Por exemplo, Windows10, MacOS, RHEL, etc.).|
|privateIpAddress|String|Privado (não roteável) endereço IPv4 ou IPv6 (consulte [RFC 1918](https://tools.ietf.org/html/rfc1918)) no momento do alerta.|
|publicIpAddress|String|Endereço IPv4 ou IPv6 roteável publicamente (consulte [RFC 1918](https://tools.ietf.org/html/rfc1918)) no momento do alerta.|
|riskScore|String|Pontuação de risco calculado/gerado pelo provedor do host.  O intervalo de valor recomendado de 0-1, que é igual a uma porcentagem.|

## <a name="json-representation"></a>Representação JSON

Veja a seguir uma representação JSON do recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.hostSecurityState"
}-->

```json
{
  "fqdn": "String",
  "isAzureAadJoined": true,
  "isAzureAadRegistered": true,
  "isHybridAzureDomainJoined": true,
  "netBiosName": "String",
  "os": "String",
  "privateIpAddress": "String",
  "publicIpAddress": "String",
  "riskScore": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "hostSecurityState resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

