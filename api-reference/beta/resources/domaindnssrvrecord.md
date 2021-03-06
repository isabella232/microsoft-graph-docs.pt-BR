---
title: tipo de recurso domainDnsSrvRecord
description: Representa um registro SRV adicionado ao arquivo de zona DNS de um domínio específico no locatário.
author: adimitui
localization_priority: Normal
ms.prod: microsoft-identity-platform
doc_type: resourcePageType
ms.openlocfilehash: 6854b30dec759726fefaf93e13ad23a49195e381
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/18/2020
ms.locfileid: "48010323"
---
# <a name="domaindnssrvrecord-resource-type"></a>tipo de recurso domainDnsSrvRecord

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Representa um registro SRV adicionado ao arquivo de zona DNS de um domínio específico no locatário. Herdado de entidade [DomainDnsRecord](domaindnsrecord.md) .

## <a name="methods"></a>Métodos
Não há suporte para consultas diretas a esse recurso. Confira o tópico de [domínio](domain.md) para obter informações sobre como consultar os registros de serviço de domínio.

## <a name="properties"></a>Propriedades
| Propriedade     | Tipo   |Descrição|
|:---------------|:--------|:----------|
|id|String| Identificador exclusivo atribuído a esta entidade. Não anulável, somente leitura.|
|IsOptional|Booliano| Se for falso, o registro SRV deverá ser configurado pelo cliente no host DNS do Microsoft Online Services para funcionar corretamente com o domínio. |
|rótulo|String| O valor usado ao configurar a propriedade *Name* do registro SRV no host DNS. |
|nameTarget|String| O valor a ser usado ao configurar a propriedade *target* do registro SRV no host DNS. |
|propor|Int32| O valor a ser usado ao configurar a propriedade *Port* do registro SRV no host DNS. |
|prioridade|Int32| O valor a ser usado ao configurar a propriedade *Priority* do registro SRV no host DNS. |
|RDP|String| O valor a ser usado ao configurar a propriedade *Protocol* do registro SRV no host DNS. |
|recordType|String|  Tipo de registro DNS. O valor é sempre *SRV*. Chave |
|service|Cadeia de caracteres| O valor a ser usado ao configurar a propriedade *Service* do registro SRV no host DNS. |
|supportedService|String| O Microsoft Online Services ou o recurso que tem uma dependência neste registro SRV.</br></br>Pode ser um dos seguintes valores: **NULL**, *email*, *SharePoint*, *EmailInternalRelayOnly*, *OfficeCommunicationsOnline*, *SharePointDefaultDomain*, *FullRedelegation*, *SharePointPublic*, *OrgIdAuthentication*, *Yammer*, *Intune* |
|TTL|Int32| O valor a ser usado ao configurar a propriedade *TTL (time-to-Live)* do registro SRV no host DNS. Não anulável |
|weight|Int32| O valor a ser usado ao configurar a propriedade *Weight* do registro SRV no host DNS. |

## <a name="relationships"></a>Relações
Nenhum


## <a name="json-representation"></a>Representação JSON
Veja a seguir uma representação JSON do recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.domainDnsSrvRecord"
}-->

```json
{
  "canonicalName": "String",
  "id": "String (identifier)",
  "isOptional": true,
  "label": "String",
  "nameTarget": "String",
  "port": 1024,
  "priority": 1024,
  "protocol": "String",
  "recordType": "String",
  "service": "String",
  "supportedService": "String",
  "ttl": 1024,
  "weight": 1024
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "domainDnsSrvRecord resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->


