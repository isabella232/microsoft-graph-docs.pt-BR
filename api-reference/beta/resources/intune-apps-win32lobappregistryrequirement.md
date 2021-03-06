---
title: tipo de recurso win32LobAppRegistryRequirement
description: Contém as propriedades do registro para detectar um aplicativo Win32
author: dougeby
localization_priority: Normal
ms.prod: intune
doc_type: resourcePageType
ms.openlocfilehash: 860bb42b4ed175310e8cd8491f242b2cb87cafd1
ms.sourcegitcommit: eb536655ffd8d49ae258664f35c50a8263238400
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/18/2020
ms.locfileid: "49280715"
---
# <a name="win32lobappregistryrequirement-resource-type"></a>tipo de recurso win32LobAppRegistryRequirement

Namespace: microsoft.graph

> **Importante:** As APIs do Microsoft Graph na versão/beta estão sujeitas a alterações; Não há suporte para o uso de produção.

> **Observação:** A API do Microsoft Graph para Intune requer uma [licença ativa do Intune](https://go.microsoft.com/fwlink/?linkid=839381) para o locatário.

Contém as propriedades do registro para detectar um aplicativo Win32


Herda de [win32LobAppRequirement](../resources/intune-apps-win32lobapprequirement.md)

## <a name="properties"></a>Propriedades
|Propriedade|Tipo|Descrição|
|:---|:---|:---|
|operator|[win32LobAppDetectionOperator](../resources/intune-apps-win32lobappdetectionoperator.md)|O operador para detecção herdada de [win32LobAppRequirement](../resources/intune-apps-win32lobapprequirement.md). Os valores possíveis são: `notConfigured`, `equal`, `notEqual`, `greaterThan`, `greaterThanOrEqual`, `lessThan`, `lessThanOrEqual`.|
|detecçaovalue|String|O valor de detecção herdado de [win32LobAppRequirement](../resources/intune-apps-win32lobapprequirement.md)|
|check32BitOn64System|Booliano|Um valor que indica se este caminho de registro é para verificar o aplicativo de 32 bits no sistema de 64 bits|
|Caminho-chave|String|O caminho da chave do registro para detectar o aplicativo de LoB (linha de negócios) do Win32|
|valueName|String|O nome do valor do registro|
|Detecção|[win32LobAppRegistryDetectionType](../resources/intune-apps-win32lobappregistrydetectiontype.md)|O tipo de detecção de dados do registro. Os possíveis valores são: `notConfigured`, `exists`, `doesNotExist`, `string`, `integer`, `version`.|

## <a name="relationships"></a>Relações
Nenhum

## <a name="json-representation"></a>Representação JSON
Veja a seguir uma representação JSON do recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.win32LobAppRegistryRequirement"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.win32LobAppRegistryRequirement",
  "operator": "String",
  "detectionValue": "String",
  "check32BitOn64System": true,
  "keyPath": "String",
  "valueName": "String",
  "detectionType": "String"
}
```




