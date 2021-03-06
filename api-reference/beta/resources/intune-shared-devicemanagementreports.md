---
title: tipo de recurso deviceManagementReports
description: Entidade singleton que atua como um contêiner para todas as funcionalidades de relatórios.
author: dougeby
localization_priority: Normal
ms.prod: intune
doc_type: resourcePageType
ms.openlocfilehash: 61ad0d59ef17cc09b65513914a4e87e390f41f0a
ms.sourcegitcommit: eb536655ffd8d49ae258664f35c50a8263238400
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/18/2020
ms.locfileid: "49336973"
---
# <a name="devicemanagementreports-resource-type"></a>tipo de recurso deviceManagementReports

Namespace: microsoft.graph

> **Importante:** As APIs do Microsoft Graph na versão/beta estão sujeitas a alterações; Não há suporte para o uso de produção.

> **Observação:** A API do Microsoft Graph para Intune requer uma [licença ativa do Intune](https://go.microsoft.com/fwlink/?linkid=839381) para o locatário.

Entidade singleton que atua como um contêiner para todas as funcionalidades de relatórios.

## <a name="methods"></a>Métodos
|Método|Tipo de retorno|Descrição|
|:---|:---|:---|
|[Obter deviceManagementReports](../api/intune-reporting-devicemanagementreports-get.md)|[deviceManagementReports](../resources/intune-shared-devicemanagementreports.md)|Leia as propriedades e as relações do objeto [deviceManagementReports](../resources/intune-shared-devicemanagementreports.md) .|
|[Atualizar deviceManagementReports](../api/intune-reporting-devicemanagementreports-update.md)|[deviceManagementReports](../resources/intune-shared-devicemanagementreports.md)|Atualiza as propriedades de um objeto [deviceManagementReports](../resources/intune-shared-devicemanagementreports.md) .|
|[ação getDeviceNonComplianceReport](../api/intune-reporting-devicemanagementreports-getdevicenoncompliancereport.md)|Fluxo|Ainda não documentado|
|[ação getPolicyNonComplianceReport](../api/intune-reporting-devicemanagementreports-getpolicynoncompliancereport.md)|Fluxo|Ainda não documentado|
|[ação getPolicyNonComplianceMetadata](../api/intune-reporting-devicemanagementreports-getpolicynoncompliancemetadata.md)|Fluxo|Ainda não documentado|
|[ação getPolicyNonComplianceSummaryReport](../api/intune-reporting-devicemanagementreports-getpolicynoncompliancesummaryreport.md)|Fluxo|Ainda não documentado|
|[ação getSettingNonComplianceReport](../api/intune-reporting-devicemanagementreports-getsettingnoncompliancereport.md)|Fluxo|Ainda não documentado|
|[ação getReportFilters](../api/intune-reporting-devicemanagementreports-getreportfilters.md)|Fluxo|Ainda não documentado|
|[ação getHistoricalReport](../api/intune-reporting-devicemanagementreports-gethistoricalreport.md)|Fluxo|Ainda não documentado|
|[ação getCachedReport](../api/intune-reporting-devicemanagementreports-getcachedreport.md)|Fluxo|Ainda não documentado|

## <a name="properties"></a>Propriedades
|Propriedade|Tipo|Descrição|
|:---|:---|:---|
|id|String|Identificador exclusivo para esta entidade|

## <a name="relationships"></a>Relações
|Relação|Tipo|Descrição|
|:---|:---|:---|
|cachedReportConfigurations|coleção [deviceManagementCachedReportConfiguration](../resources/intune-reporting-devicemanagementcachedreportconfiguration.md)|Entidade que representa a configuração de um relatório em cache|
|exportJobs|coleção [deviceManagementExportJob](../resources/intune-reporting-devicemanagementexportjob.md)|Entidade que representa um trabalho para exportar um relatório|
|reportSchedules|coleção [deviceManagementReportSchedule](../resources/intune-reporting-devicemanagementreportschedule.md)|Entidade que representa um cronograma para o qual os relatórios são entregues|

## <a name="json-representation"></a>Representação JSON
Veja a seguir uma representação JSON do recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.deviceManagementReports"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceManagementReports",
  "id": "String (identifier)"
}
```




