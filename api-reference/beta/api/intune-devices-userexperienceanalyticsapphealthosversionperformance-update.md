---
title: Atualizar userExperienceAnalyticsAppHealthOSVersionPerformance
description: Atualiza as propriedades de um objeto userExperienceAnalyticsAppHealthOSVersionPerformance.
author: dougeby
localization_priority: Normal
ms.prod: intune
doc_type: apiPageType
ms.openlocfilehash: 969b89d16d9ab265246c0bca39932d874675da5f
ms.sourcegitcommit: eb536655ffd8d49ae258664f35c50a8263238400
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/18/2020
ms.locfileid: "49202525"
---
# <a name="update-userexperienceanalyticsapphealthosversionperformance"></a>Atualizar userExperienceAnalyticsAppHealthOSVersionPerformance

Namespace: microsoft.graph

> **Importante:** As APIs do Microsoft Graph na versão/beta estão sujeitas a alterações; Não há suporte para o uso de produção.

> **Observação:** A API do Microsoft Graph para Intune requer uma [licença ativa do Intune](https://go.microsoft.com/fwlink/?linkid=839381) para o locatário.

Atualiza as propriedades de um objeto [userExperienceAnalyticsAppHealthOSVersionPerformance](../resources/intune-devices-userexperienceanalyticsapphealthosversionperformance.md) .

## <a name="prerequisites"></a>Pré-requisitos
Uma das seguintes permissões é obrigatória para chamar esta API. Para saber mais, incluindo como escolher permissões, confira [Permissões](/graph/permissions-reference).

|Tipo de permissão|Permissões (de privilégios máximos a mínimos)|
|:---|:---|
|Delegada (conta corporativa ou de estudante)|DeviceManagementManagedDevices.ReadWrite.All|
|Delegada (conta pessoal da Microsoft)|Sem suporte.|
|Application|DeviceManagementManagedDevices.ReadWrite.All|

## <a name="http-request"></a>Solicitação HTTP
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/userExperienceAnalyticsAppHealthOSVersionPerformance/{userExperienceAnalyticsAppHealthOSVersionPerformanceId}
```

## <a name="request-headers"></a>Cabeçalhos de solicitação
|Cabeçalho|Valor|
|:---|:---|
|Autorização|&lt;Token&gt; de portador obrigatório.|
|Aceitar|application/json|

## <a name="request-body"></a>Corpo da solicitação
No corpo da solicitação, forneça uma representação JSON do objeto [userExperienceAnalyticsAppHealthOSVersionPerformance](../resources/intune-devices-userexperienceanalyticsapphealthosversionperformance.md) .

A tabela a seguir mostra as propriedades que são necessárias ao criar [userExperienceAnalyticsAppHealthOSVersionPerformance](../resources/intune-devices-userexperienceanalyticsapphealthosversionperformance.md).

|Propriedade|Tipo|Descrição|
|:---|:---|:---|
|id|String|O identificador exclusivo do objeto de desempenho da versão da experiência do usuário do Analytics OS.|
|osVersion|String|A versão do sistema operacional instalada no dispositivo.|
|osBuildNumber|String|O número de compilação do sistema operacional instalado no dispositivo.|
|activeDeviceCount|Int32|O número de dispositivos ativos para a versão do sistema operacional. Valores válidos-2147483648 a 2147483647|
|meanTimeToFailureInMinutes|Int32|O tempo médio de falha para a versão do sistema operacional em minutos. Valores válidos-2147483648 a 2147483647|
|osVersionAppHealthScore|Duplo|A pontuação de integridade do aplicativo da versão do sistema operacional. Valores válidos-1.79769313486232 E + 308 a 1.79769313486232 E + 308|
|osVersionAppHealthStatus|String|O status de integridade geral do aplicativo da versão do sistema operacional.|



## <a name="response"></a>Resposta
Se tiver êxito, este método retornará um `200 OK` código de resposta e um objeto [userExperienceAnalyticsAppHealthOSVersionPerformance](../resources/intune-devices-userexperienceanalyticsapphealthosversionperformance.md) atualizado no corpo da resposta.

## <a name="example"></a>Exemplo

### <a name="request"></a>Solicitação
Este é um exemplo da solicitação.
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/userExperienceAnalyticsAppHealthOSVersionPerformance/{userExperienceAnalyticsAppHealthOSVersionPerformanceId}
Content-type: application/json
Content-length: 357

{
  "@odata.type": "#microsoft.graph.userExperienceAnalyticsAppHealthOSVersionPerformance",
  "osVersion": "Os Version value",
  "osBuildNumber": "Os Build Number value",
  "activeDeviceCount": 1,
  "meanTimeToFailureInMinutes": 10,
  "osVersionAppHealthScore": 7.666666666666667,
  "osVersionAppHealthStatus": "Os Version App Health Status value"
}
```

### <a name="response"></a>Resposta
Veja a seguir um exemplo da resposta. Observação: o objeto response mostrado aqui pode estar truncado por motivos de concisão. Todas as propriedades serão retornadas de uma chamada real.
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 406

{
  "@odata.type": "#microsoft.graph.userExperienceAnalyticsAppHealthOSVersionPerformance",
  "id": "7c28e16b-e16b-7c28-6be1-287c6be1287c",
  "osVersion": "Os Version value",
  "osBuildNumber": "Os Build Number value",
  "activeDeviceCount": 1,
  "meanTimeToFailureInMinutes": 10,
  "osVersionAppHealthScore": 7.666666666666667,
  "osVersionAppHealthStatus": "Os Version App Health Status value"
}
```




