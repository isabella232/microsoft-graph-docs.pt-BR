---
title: Tipo de recurso omaSettingStringXml
description: Definição de StringXML para configurações de OMA.
author: dougeby
localization_priority: Normal
ms.prod: intune
doc_type: resourcePageType
ms.openlocfilehash: b4ac7c46dd21ffb9e9a31223822cf304e2b80c4f
ms.sourcegitcommit: eb536655ffd8d49ae258664f35c50a8263238400
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/18/2020
ms.locfileid: "49215720"
---
# <a name="omasettingstringxml-resource-type"></a>Tipo de recurso omaSettingStringXml

Namespace: microsoft.graph

> **Importante:** As APIs do Microsoft Graph na versão/beta estão sujeitas a alterações; Não há suporte para o uso de produção.

> **Observação:** A API do Microsoft Graph para Intune requer uma [licença ativa do Intune](https://go.microsoft.com/fwlink/?linkid=839381) para o locatário.

Definição de StringXML para configurações de OMA.


Herda de [omaSetting](../resources/intune-deviceconfig-omasetting.md)

## <a name="properties"></a>Propriedades
|Propriedade|Tipo|Descrição|
|:---|:---|:---|
|displayName|String|Nome de exibição. Herda de [omaSetting](../resources/intune-deviceconfig-omasetting.md)|
|description|String|Descrição. Herda de [omaSetting](../resources/intune-deviceconfig-omasetting.md)|
|omaUri|Cadeia de caracteres|OMA. Herda de [omaSetting](../resources/intune-deviceconfig-omasetting.md)|
|isEncrypted|Boolean|Indica se o campo de valor é criptografado. Herda de [omaSetting](../resources/intune-deviceconfig-omasetting.md)|
|fileName|Cadeia de caracteres|Nome do arquivo associado à propriedade de valor (*.xml).|
|valor|Binário|Valor. (Matriz de bytes codificados de UTF8)|

## <a name="relationships"></a>Relações
Nenhum

## <a name="json-representation"></a>Representação JSON
Veja a seguir uma representação JSON do recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.omaSettingStringXml"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.omaSettingStringXml",
  "displayName": "String",
  "description": "String",
  "omaUri": "String",
  "isEncrypted": true,
  "fileName": "String",
  "value": "binary"
}
```




