---
title: tipo de recurso win32LobAppRegistryRule
description: Um tipo complexo para armazenar dados de regra de registro para um aplicativo LOB Win32.
author: dougeby
localization_priority: Normal
ms.prod: intune
doc_type: resourcePageType
ms.openlocfilehash: 64343873093428849462cbdc12fc078a7a028e2d
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/18/2020
ms.locfileid: "48080035"
---
# <a name="win32lobappregistryrule-resource-type"></a>tipo de recurso win32LobAppRegistryRule

Namespace: microsoft.graph

> **Observação:** A API do Microsoft Graph para Intune requer uma [licença ativa do Intune](https://go.microsoft.com/fwlink/?linkid=839381) para o locatário.

Um tipo complexo para armazenar dados de regra de registro para um aplicativo LOB Win32.


Herda de [win32LobAppRule](../resources/intune-apps-win32lobapprule.md)

## <a name="properties"></a>Propriedades
|Propriedade|Tipo|Descrição|
|:---|:---|:---|
|ruleType|[win32LobAppRuleType](../resources/intune-apps-win32lobappruletype.md)|O tipo de regra que indica o objetivo da regra. Herdado de [win32LobAppRule](../resources/intune-apps-win32lobapprule.md). Os valores possíveis são: `detection` e `requirement`.|
|check32BitOn64System|Booliano|Um valor que indica se é para pesquisar o registro de 32 bits em sistemas de 64 bits.|
|Caminho-chave|Cadeia de caracteres|O caminho completo da entrada de registro que contém o valor a ser detectado.|
|valueName|Cadeia de caracteres|O nome do valor do registro a ser detectado.|
|OperationType|[win32LobAppRegistryRuleOperationType](../resources/intune-apps-win32lobappregistryruleoperationtype.md)|O tipo de operação do registro. Os possíveis valores são: `notConfigured`, `exists`, `doesNotExist`, `string`, `integer`, `version`.|
|operator|[win32LobAppRuleOperator](../resources/intune-apps-win32lobappruleoperator.md)|O operador para detecção de registro. Os valores possíveis são: `notConfigured`, `equal`, `notEqual`, `greaterThan`, `greaterThanOrEqual`, `lessThan`, `lessThanOrEqual`.|
|ComparisonValue|Cadeia de caracteres|O valor de comparação do registro.|

## <a name="relationships"></a>Relações
Nenhum

## <a name="json-representation"></a>Representação JSON
Veja a seguir uma representação JSON do recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.win32LobAppRegistryRule"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.win32LobAppRegistryRule",
  "ruleType": "String",
  "check32BitOn64System": true,
  "keyPath": "String",
  "valueName": "String",
  "operationType": "String",
  "operator": "String",
  "comparisonValue": "String"
}
```





