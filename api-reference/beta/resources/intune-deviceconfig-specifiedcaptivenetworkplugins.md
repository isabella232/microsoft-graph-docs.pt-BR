---
title: tipo de recurso specifiedCaptiveNetworkPlugins
description: Especifica todos os plugins de rede prisioneiros permitidos durante a conexão VPN AlwaysOn do IKEv2
author: dougeby
localization_priority: Normal
ms.prod: intune
doc_type: resourcePageType
ms.openlocfilehash: 107c700a35e24cf47b9af2642523ed9b1c735d26
ms.sourcegitcommit: eb536655ffd8d49ae258664f35c50a8263238400
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/18/2020
ms.locfileid: "49276592"
---
# <a name="specifiedcaptivenetworkplugins-resource-type"></a>tipo de recurso specifiedCaptiveNetworkPlugins

Namespace: microsoft.graph

> **Importante:** As APIs do Microsoft Graph na versão/beta estão sujeitas a alterações; Não há suporte para o uso de produção.

> **Observação:** A API do Microsoft Graph para Intune requer uma [licença ativa do Intune](https://go.microsoft.com/fwlink/?linkid=839381) para o locatário.

Especifica todos os plugins de rede prisioneiros permitidos durante a conexão VPN AlwaysOn do IKEv2

## <a name="properties"></a>Propriedades
|Propriedade|Tipo|Descrição|
|:---|:---|:---|
|allowedBundleIdentifiers|Coleção de cadeias de caracteres|Endereço do servidor IKEv2. Deve ser um FQDN, userfqdn, endereço de rede ou ASN1DN|

## <a name="relationships"></a>Relações
Nenhum

## <a name="json-representation"></a>Representação JSON
Veja a seguir uma representação JSON do recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.specifiedCaptiveNetworkPlugins"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.specifiedCaptiveNetworkPlugins",
  "allowedBundleIdentifiers": [
    "String"
  ]
}
```




