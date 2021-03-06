---
title: tipo de recurso detailsInfo
description: Um conjunto de propriedades que pode conter qualquer informação sobre a identidade ou o sistema associado.
localization_priority: Normal
author: khotz
ms.prod: microsoft-identity-platform
doc_type: resourcePageType
ms.openlocfilehash: c08dcb867f92bd65449be891bf0ae0e8a12a2459
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/18/2020
ms.locfileid: "48049868"
---
# <a name="detailsinfo-resource-type"></a>tipo de recurso detailsInfo

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Um conjunto de propriedades que pode conter qualquer informação sobre a identidade ou o sistema associado. Isso pode incluir detalhes sobre a propriedade que está sendo provisionada ou o sistema de origem/destino.

## <a name="properties"></a>Propriedades
O recurso **detailsInfo** é uma cadeia de caracteres JSON que contém propriedades adicionais como **ApplicationId**, **ObjectID**e **UPN**. O conjunto de propriedades varia com base no tipo de recurso que está sendo provisionado. [List provisioningObjectSummary](../api/provisioningobjectsummary-list.md) mostra um exemplo disso.

## <a name="relationships"></a>Relações
Nenhum
## <a name="json-representation"></a>Representação JSON
Veja a seguir uma representação JSON do recurso.
<!--{
  "blockType": "resource",
  "@odata.type": "microsoft.graph.detailsInfo",
  "openType": true,
 "optionalProperties": [
 
 ],
}-->
``` json
{
  "@odata.type": "microsoft.graph.detailsInfo"
}
```


