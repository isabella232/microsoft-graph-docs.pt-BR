---
title: Tipo de recurso deviceComplianceScheduledActionForRule
description: Ação agendada para a regra
author: dougeby
localization_priority: Normal
ms.prod: intune
doc_type: resourcePageType
ms.openlocfilehash: 391017a3ded43f40286b841594e80e773294e7a5
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/18/2020
ms.locfileid: "48003238"
---
# <a name="devicecompliancescheduledactionforrule-resource-type"></a>Tipo de recurso deviceComplianceScheduledActionForRule

Namespace: microsoft.graph

> **Observação:** A API do Microsoft Graph para Intune requer uma [licença ativa do Intune](https://go.microsoft.com/fwlink/?linkid=839381) para o locatário.

Ação agendada para a regra

## <a name="methods"></a>Methods
|Método|Tipo de retorno|Descrição|
|:---|:---|:---|
|[Listar deviceComplianceScheduledActionForRules](../api/intune-deviceconfig-devicecompliancescheduledactionforrule-list.md)|Conjunto [deviceComplianceScheduledActionForRule](../resources/intune-deviceconfig-devicecompliancescheduledactionforrule.md)|Listar propriedades e relações de objetos de [deviceComplianceScheduledActionForRule](../resources/intune-deviceconfig-devicecompliancescheduledactionforrule.md).|
|[Obter deviceComplianceScheduledActionForRule](../api/intune-deviceconfig-devicecompliancescheduledactionforrule-get.md)|[deviceComplianceScheduledActionForRule](../resources/intune-deviceconfig-devicecompliancescheduledactionforrule.md)|Ler propriedades e relações de objetos de [deviceComplianceScheduledActionForRule](../resources/intune-deviceconfig-devicecompliancescheduledactionforrule.md).|
|[Criar deviceComplianceScheduledActionForRule](../api/intune-deviceconfig-devicecompliancescheduledactionforrule-create.md)|[deviceComplianceScheduledActionForRule](../resources/intune-deviceconfig-devicecompliancescheduledactionforrule.md)|Criar um novo objeto de [deviceComplianceScheduledActionForRule](../resources/intune-deviceconfig-devicecompliancescheduledactionforrule.md).|
|[Excluir deviceComplianceScheduledActionForRule](../api/intune-deviceconfig-devicecompliancescheduledactionforrule-delete.md)|Nenhum|Exclui [deviceComplianceScheduledActionForRule](../resources/intune-deviceconfig-devicecompliancescheduledactionforrule.md).|
|[Atualizar deviceComplianceScheduledActionForRule](../api/intune-deviceconfig-devicecompliancescheduledactionforrule-update.md)|[deviceComplianceScheduledActionForRule](../resources/intune-deviceconfig-devicecompliancescheduledactionforrule.md)|Atualizar as propriedades de um objeto de [deviceComplianceScheduledActionForRule](../resources/intune-deviceconfig-devicecompliancescheduledactionforrule.md).|

## <a name="properties"></a>Propriedades
|Propriedade|Tipo|Descrição|
|:---|:---|:---|
|id|String|Chave da entidade.|
|ruleName|Cadeia de caracteres|Nome da regra à qual essa ação agendada se aplica.|

## <a name="relationships"></a>Relações
|Relação|Tipo|Descrição|
|:---|:---|:---|
|scheduledActionConfigurations|Conjunto [deviceComplianceActionItem](../resources/intune-deviceconfig-devicecomplianceactionitem.md)|A lista de configurações de ações agendadas para essa política de conformidade.|

## <a name="json-representation"></a>Representação JSON
Veja a seguir uma representação JSON do recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.deviceComplianceScheduledActionForRule"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceComplianceScheduledActionForRule",
  "id": "String (identifier)",
  "ruleName": "String"
}
```









