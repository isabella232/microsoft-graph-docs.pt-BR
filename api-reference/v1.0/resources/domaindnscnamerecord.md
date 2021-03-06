---
title: tipo de recurso domainDnsCnameRecord
description: Representa um registro CNAME adicionado ao arquivo de zona DNS de um domínio específico no locatário.
author: adimitui
localization_priority: Normal
ms.prod: microsoft-identity-platform
doc_type: resourcePageType
ms.openlocfilehash: 9d2182ed121dbf303e3f9982c53655cecb6f4c10
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/18/2020
ms.locfileid: "48091716"
---
# <a name="domaindnscnamerecord-resource-type"></a>tipo de recurso domainDnsCnameRecord

Namespace: microsoft.graph

Representa um registro CNAME adicionado ao arquivo de zona DNS de um domínio específico no locatário. Herdado de entidade [DomainDnsRecord](domaindnsrecord.md) .


## <a name="methods"></a>Métodos
Não há suporte para consultas diretas a esse recurso. Confira o tópico de [domínio](domain.md) para obter informações sobre como consultar os registros de serviço de domínio.

## <a name="properties"></a>Propriedades
| Propriedade     | Tipo   |Descrição|
|:---------------|:--------|:----------|
|canônicaname|Cadeia de caracteres| O nome canônico do registro CNAME. Usado para configurar o registro CNAME no host DNS. |
|id|Cadeia de caracteres| Identificador exclusivo atribuído a esta entidade. Não anulável, somente leitura|
|IsOptional|Booliano| Se for falso, o registro CNAME deverá ser configurado pelo cliente no host DNS do Microsoft Online Services para funcionar corretamente com o domínio. Não anulável |
|rótulo|Cadeia de caracteres| O valor usado ao configurar o *alias/host/nome* do registro CNAME no host DNS. |
|recordType|Cadeia de caracteres| Tipo de registro DNS. O valor é sempre *CNAME*. Chave|
|supportedService|Cadeia de caracteres| O Microsoft Online Services ou o recurso que tem uma dependência neste registro CNAME.</br></br>Pode ser um dos seguintes valores: **NULL**, *email*, *SharePoint*, *EmailInternalRelayOnly*, *OfficeCommunicationsOnline*, *SharePointDefaultDomain*, *FullRedelegation*, *SharePointPublic*, *OrgIdAuthentication*, *Yammer*, *Intune*|
|TTL|Int32| O valor a ser usado ao configurar a propriedade TTL (time-to-Live) do registro CNAME no host DNS. Não anulável |

## <a name="relationships"></a>Relações
Nenhum


## <a name="json-representation"></a>Representação JSON
Veja a seguir uma representação JSON do recurso.

<!-- {
  "blockType": "resource",
  "baseType": "microsoft.graph.domainDnsRecord",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.domainDnsCnameRecord"
}-->

```json
{
  "canonicalName": "String",
  "id": "String (identifier)",
  "isOptional": true,
  "label": "String",
  "recordType": "String",
  "supportedService": "String",
  "ttl": 1024
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "domainDnsCnameRecord resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

