---
title: Criar groupPolicyMigrationReport
description: Criar um novo objeto groupPolicyMigrationReport.
author: dougeby
localization_priority: Normal
ms.prod: intune
doc_type: apiPageType
ms.openlocfilehash: e6b63022cc67ad0f5d6e51bf3eec3f7dd2272839
ms.sourcegitcommit: eb536655ffd8d49ae258664f35c50a8263238400
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/18/2020
ms.locfileid: "49263117"
---
# <a name="create-grouppolicymigrationreport"></a>Criar groupPolicyMigrationReport

Namespace: microsoft.graph

> **Importante:** As APIs do Microsoft Graph na versão/beta estão sujeitas a alterações; Não há suporte para o uso de produção.

> **Observação:** A API do Microsoft Graph para Intune requer uma [licença ativa do Intune](https://go.microsoft.com/fwlink/?linkid=839381) para o locatário.

Criar um novo objeto [groupPolicyMigrationReport](../resources/intune-gpanalyticsservice-grouppolicymigrationreport.md) .

## <a name="prerequisites"></a>Pré-requisitos
Uma das seguintes permissões é obrigatória para chamar esta API. Para saber mais, incluindo como escolher permissões, confira [Permissões](/graph/permissions-reference).

|Tipo de permissão|Permissões (de privilégios máximos a mínimos)|
|:---|:---|
|Delegado (conta corporativa ou de estudante)|DeviceManagementConfiguration.ReadWrite.All|
|Delegado (conta pessoal da Microsoft)|Sem suporte.|
|Aplicativo|DeviceManagementConfiguration.ReadWrite.All|

## <a name="http-request"></a>Solicitação HTTP
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/groupPolicyMigrationReports
```

## <a name="request-headers"></a>Cabeçalhos de solicitação
|Cabeçalho|Valor|
|:---|:---|
|Autorização|&lt;Token&gt; de portador obrigatório.|
|Aceitar|application/json|

## <a name="request-body"></a>Corpo da solicitação
No corpo da solicitação, forneça uma representação JSON do objeto groupPolicyMigrationReport.

A tabela a seguir mostra as propriedades que são necessárias ao criar groupPolicyMigrationReport.

|Propriedade|Tipo|Descrição|
|:---|:---|:---|
|id|String|Ainda não documentado|
|groupPolicyObjectId|Guid|O GUID do objeto da política de grupo do conteúdo XML do GPO|
|displayName|String|O nome do objeto de diretiva de grupo do conteúdo XML do GPO|
|ouDistinguishedName|String|O nome diferenciado da OU.|
|createdDateTime|DateTimeOffset|A data e a hora em que o GroupPolicyMigrationReport foi criado.|
|lastModifiedDateTime|DateTimeOffset|A data e a hora em que o GroupPolicyMigrationReport foi modificado pela última vez.|
|groupPolicyCreatedDateTime|DateTimeOffset|A data e a hora em que o GroupPolicyMigrationReport foi criado.|
|groupPolicyLastModifiedDateTime|DateTimeOffset|A data e a hora em que o GroupPolicyMigrationReport foi modificado pela última vez.|
|migrationReadiness|[groupPolicyMigrationReadiness](../resources/intune-gpanalyticsservice-grouppolicymigrationreadiness.md)|A cobertura do Intune para o arquivo de objeto de diretiva de grupo associado. Os valores possíveis são: `none`, `partial`, `complete`, `error`, `notApplicable`.|
|targetedInActiveDirectory|Booliano|A propriedade de destino no AD do conteúdo XML do GPO|
|totalSettingsCount|Int32|O número total de configurações de política de grupo do arquivo de GPO.|
|supportedSettingsCount|Int32|O número de configurações de política de grupo compatíveis com o Intune.|
|supportedSettingsPercent|Int32|A porcentagem de configurações de política de grupo compatíveis com o Intune.|



## <a name="response"></a>Resposta
Se tiver êxito, este método retornará um `201 Created` código de resposta e um objeto [groupPolicyMigrationReport](../resources/intune-gpanalyticsservice-grouppolicymigrationreport.md) no corpo da resposta.

## <a name="example"></a>Exemplo

### <a name="request"></a>Solicitação
Este é um exemplo da solicitação.
``` http
POST https://graph.microsoft.com/beta/deviceManagement/groupPolicyMigrationReports
Content-type: application/json
Content-length: 544

{
  "@odata.type": "#microsoft.graph.groupPolicyMigrationReport",
  "groupPolicyObjectId": "ca1c97af-97af-ca1c-af97-1ccaaf971cca",
  "displayName": "Display Name value",
  "ouDistinguishedName": "Ou Distinguished Name value",
  "groupPolicyCreatedDateTime": "2016-12-31T23:58:14.0676812-08:00",
  "groupPolicyLastModifiedDateTime": "2017-01-01T00:02:51.2241017-08:00",
  "migrationReadiness": "partial",
  "targetedInActiveDirectory": true,
  "totalSettingsCount": 2,
  "supportedSettingsCount": 6,
  "supportedSettingsPercent": 8
}
```

### <a name="response"></a>Resposta
Veja a seguir um exemplo da resposta. Observação: o objeto response mostrado aqui pode estar truncado por motivos de concisão. Todas as propriedades serão retornadas de uma chamada real.
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 716

{
  "@odata.type": "#microsoft.graph.groupPolicyMigrationReport",
  "id": "60663fa8-3fa8-6066-a83f-6660a83f6660",
  "groupPolicyObjectId": "ca1c97af-97af-ca1c-af97-1ccaaf971cca",
  "displayName": "Display Name value",
  "ouDistinguishedName": "Ou Distinguished Name value",
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "groupPolicyCreatedDateTime": "2016-12-31T23:58:14.0676812-08:00",
  "groupPolicyLastModifiedDateTime": "2017-01-01T00:02:51.2241017-08:00",
  "migrationReadiness": "partial",
  "targetedInActiveDirectory": true,
  "totalSettingsCount": 2,
  "supportedSettingsCount": 6,
  "supportedSettingsPercent": 8
}
```




