---
title: Tipo de recurso deviceCompliancePolicySettingState
description: Estado da configuração da política de conformidade de dispositivo para um determinado dispositivo.
author: dougeby
localization_priority: Normal
ms.prod: intune
doc_type: resourcePageType
ms.openlocfilehash: a15aa7494c4580c1b69eebf7499066a153ce7f63
ms.sourcegitcommit: eb536655ffd8d49ae258664f35c50a8263238400
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/18/2020
ms.locfileid: "49260338"
---
# <a name="devicecompliancepolicysettingstate-resource-type"></a>Tipo de recurso deviceCompliancePolicySettingState

Namespace: microsoft.graph

> **Importante:** As APIs do Microsoft Graph na versão/beta estão sujeitas a alterações; Não há suporte para o uso de produção.

> **Observação:** A API do Microsoft Graph para Intune requer uma [licença ativa do Intune](https://go.microsoft.com/fwlink/?linkid=839381) para o locatário.

Estado da configuração da política de conformidade de dispositivo para um determinado dispositivo.

## <a name="properties"></a>Propriedades
|Propriedade|Tipo|Descrição|
|:---|:---|:---|
|configuração|Cadeia de caracteres|A configuração que é relatada|
|settingName|Cadeia de caracteres|Nome de configuração localizada/de usuário que é relatada|
|instanceDisplayName|Cadeia de caracteres|Nome da instância de configuração que é relatada.|
|state|[complianceStatus](../resources/intune-shared-compliancestatus.md)|O estado de conformidade da configuração. Os valores possíveis são: `unknown`, `notApplicable`, `compliant`, `remediated`, `nonCompliant`, `error`, `conflict`, `notAssigned`.|
|errorCode|Int64|Código de erro da configuração|
|errorDescription|Cadeia de caracteres|Descrição de erro|
|userId|Cadeia de caracteres|UserId|
|userName|Cadeia de caracteres|UserName|
|userEmail|Cadeia de caracteres|UserEmail|
|userPrincipalName|String|UserPrincipalName.|
|fontes|Conjunto [settingSource](../resources/intune-deviceconfig-settingsource.md)|Políticas de colaboração|
|currentValue|Cadeia de caracteres|Valor atual da configuração em um dispositivo|
|settingInstanceId|String|SettingInstanceId|

## <a name="relationships"></a>Relações
Nenhum

## <a name="json-representation"></a>Representação JSON
Veja a seguir uma representação JSON do recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.deviceCompliancePolicySettingState"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceCompliancePolicySettingState",
  "setting": "String",
  "settingName": "String",
  "instanceDisplayName": "String",
  "state": "String",
  "errorCode": 1024,
  "errorDescription": "String",
  "userId": "String",
  "userName": "String",
  "userEmail": "String",
  "userPrincipalName": "String",
  "sources": [
    {
      "@odata.type": "microsoft.graph.settingSource",
      "id": "String",
      "displayName": "String",
      "sourceType": "String"
    }
  ],
  "currentValue": "String",
  "settingInstanceId": "String"
}
```




