---
title: tipo de recurso domainDnsMxRecord
description: Representa um registro MX adicionado ao arquivo de zona DNS de um domínio específico no locatário.
author: adimitui
localization_priority: Normal
ms.prod: microsoft-identity-platform
doc_type: resourcePageType
ms.openlocfilehash: 0b77369b05bdd3de2e1141066aef4d3d4ddfa8ae
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/18/2020
ms.locfileid: "48091709"
---
# <a name="domaindnsmxrecord-resource-type"></a>tipo de recurso domainDnsMxRecord

Namespace: microsoft.graph

Representa um registro MX adicionado ao arquivo de zona DNS de um domínio específico no locatário. Herdado de entidade [DomainDnsRecord](domaindnsrecord.md) .

## <a name="methods"></a>Métodos
Não há suporte para consultas diretas a esse recurso. Confira o tópico de [domínio](domain.md) para obter informações sobre como consultar os registros de serviço de domínio.

## <a name="properties"></a>Propriedades
| Propriedade     | Tipo   |Descrição|
|:---------------|:--------|:----------|
|id|Cadeia de caracteres| Identificador exclusivo atribuído a esta entidade. Não anulável, somente leitura.|
|IsOptional|Booliano| Se for falso, o registro MX deve ser configurado pelo cliente no host DNS do Microsoft Online Services para funcionar corretamente com o domínio. |
|rótulo|Cadeia de caracteres| O valor usado ao configurar a propriedade *alias/Host/Name* do registro MX no host DNS. |
|mailExchange|Cadeia de caracteres| O valor usado ao configurar a *resposta/destino/valor* do registro MX no host DNS.|
|preferência|Int32| O valor usado ao configurar a propriedade *preference/Priority* do registro MX no host DNS. |
|recordType|Cadeia de caracteres| Tipo de registro DNS. O valor é sempre *MX*. Chave |
|supportedService|Cadeia de caracteres| O Microsoft Online Services ou o recurso que tem uma dependência neste registro MX.</br></br>Pode ser um dos seguintes valores: **NULL**, *email*, *SharePoint*, *EmailInternalRelayOnly*, *OfficeCommunicationsOnline*, *SharePointDefaultDomain*, *FullRedelegation*, *SharePointPublic*, *OrgIdAuthentication*, *Yammer*, *Intune* |
|TTL|Int32| O valor a ser usado ao configurar a propriedade *TTL (time-to-Live)* do registro MX no host DNS. Não anulável |

## <a name="relationships"></a>Relações
Nenhum

## <a name="json-representation"></a>Representação JSON
Veja a seguir uma representação JSON do recurso.

<!-- {
  "blockType": "resource",
  "baseType": "microsoft.graph.domainDnsRecord",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.domainDnsMxRecord"
}-->

```json
{
  "id": "String (identifier)",
  "isOptional": true,
  "label": "String",
  "mailExchange": "String",
  "preference": 1024,
  "recordType": "String",
  "supportedService": "String",
  "ttl": 1024
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "domainDnsMxRecord resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

