---
title: tipo de recurso verifiedCustomDomainCertificatesMetadata
description: Representa os metadados de criar certificado personalizados para um aplicativo local publicado por meio do proxy de aplicativo.
localization_priority: Normal
author: japere
ms.prod: microsoft-identity-platform
doc_type: resourcePageType
ms.openlocfilehash: 4f3dc4cbe1a68ae6f7c751c9b305f95901928d17
ms.sourcegitcommit: 7ceec757fd82ef3fd80aa3089ef46d3807aa3aa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2020
ms.locfileid: "48402944"
---
# <a name="verifiedcustomdomaincertificatesmetadata-resource-type"></a>tipo de recurso verifiedCustomDomainCertificatesMetadata

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Representa os metadados do certificado de domínio personalizado para o recurso [onPremisesPublishing](onpremisespublishing.md) ao publicar um aplicativo local com o proxy de aplicativo. Usar um domínio personalizado permite que você use seu próprio nome de domínio em vez do domínio padrão, msappproxy.net, para seu aplicativo. Para saber mais, confira [domínios personalizados no proxy de aplicativo do Azure ad](/azure/active-directory/manage-apps/application-proxy-configure-custom-domain).

## <a name="properties"></a>Propriedades

| Propriedade     | Tipo        | Descrição |
|:-------------|:------------|:------------|
|expiryDate|DateTimeOffset| A data de expiração do certificado de domínio personalizado. O tipo Timestamp representa informações de data e hora usando o formato ISO 8601 e está sempre no horário UTC. Por exemplo, meia-noite em UTC no dia 1º de janeiro de 2014 teria esta aparência: `'2014-01-01T00:00:00Z'`. |
|Emitido|DateTimeOffset| A data de emissão do domínio personalizado. O tipo Timestamp representa informações de data e hora usando o formato ISO 8601 e está sempre no horário UTC. Por exemplo, meia-noite em UTC no dia 1º de janeiro de 2014 teria esta aparência: `'2014-01-01T00:00:00Z'`. |
|issuerName|Cadeia de caracteres| O nome do emissor do certificado de domínio personalizado. |
|SubjectName|Cadeia de caracteres| O nome da entidade do certificado de domínio personalizado. |
|identificação|Cadeia de caracteres| A impressão digital associada ao certificado de domínio personalizado. |

## <a name="json-representation"></a>Representação JSON

Veja a seguir uma representação JSON do recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.verifiedCustomDomainCertificatesMetadata",
  "baseType": null
}-->

```json
{
  "expiryDate": "String (timestamp)",
  "issueDate": "String (timestamp)",
  "issuerName": "String",
  "subjectName": "String",
  "thumbprint": "String"
}
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "verifiedCustomDomainCertificatesMetadata resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->