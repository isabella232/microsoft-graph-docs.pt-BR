---
title: Obter windowsAutopilotDeploymentProfile
description: Leia as propriedades e as relações do objeto windowsAutopilotDeploymentProfile.
author: rolyon
localization_priority: Normal
ms.prod: Intune
doc_type: apiPageType
ms.openlocfilehash: 329cf563d5df9f97d1bd1ad648a02ebbff284056
ms.sourcegitcommit: 86903a4730bbd825eabb7f0a1b2429723cc8b1e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/26/2019
ms.locfileid: "37199381"
---
# <a name="get-windowsautopilotdeploymentprofile"></a><span data-ttu-id="8d7a0-103">Obter windowsAutopilotDeploymentProfile</span><span class="sxs-lookup"><span data-stu-id="8d7a0-103">Get windowsAutopilotDeploymentProfile</span></span>

> <span data-ttu-id="8d7a0-104">**Importante:** As APIs do Microsoft Graph na versão/beta estão sujeitas a alterações; Não há suporte para o uso de produção.</span><span class="sxs-lookup"><span data-stu-id="8d7a0-104">**Important:** Microsoft Graph APIs under the /beta version are subject to change; production use is not supported.</span></span>

> <span data-ttu-id="8d7a0-105">**Observação:** A API do Microsoft Graph para Intune requer uma [licença do Active Intune](https://go.microsoft.com/fwlink/?linkid=839381) para o locatário.</span><span class="sxs-lookup"><span data-stu-id="8d7a0-105">**Note:** The Microsoft Graph API for Intune requires an [active Intune license](https://go.microsoft.com/fwlink/?linkid=839381) for the tenant.</span></span>

<span data-ttu-id="8d7a0-106">Leia as propriedades e as relações do objeto [windowsAutopilotDeploymentProfile](../resources/intune-shared-windowsautopilotdeploymentprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="8d7a0-106">Read properties and relationships of the [windowsAutopilotDeploymentProfile](../resources/intune-shared-windowsautopilotdeploymentprofile.md) object.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="8d7a0-107">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="8d7a0-107">Prerequisites</span></span>
<span data-ttu-id="8d7a0-p101">Uma das seguintes permissões é obrigatória para chamar esta API. Para saber mais, incluindo como escolher permissões, confira [Permissões](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="8d7a0-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="8d7a0-110">Tipo de permissão</span><span class="sxs-lookup"><span data-stu-id="8d7a0-110">Permission type</span></span>|<span data-ttu-id="8d7a0-111">Permissões (de privilégios máximos a mínimos)</span><span class="sxs-lookup"><span data-stu-id="8d7a0-111">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="8d7a0-112">Delegado (conta corporativa ou de estudante)</span><span class="sxs-lookup"><span data-stu-id="8d7a0-112">Delegated (work or school account)</span></span>||
| <span data-ttu-id="8d7a0-113">&nbsp;&nbsp; **Registro**</span><span class="sxs-lookup"><span data-stu-id="8d7a0-113">&nbsp; &nbsp; **Enrollment**</span></span> | <span data-ttu-id="8d7a0-114">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span><span class="sxs-lookup"><span data-stu-id="8d7a0-114">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span></span>|
| <span data-ttu-id="8d7a0-115">&nbsp;&nbsp; **Conjunto de políticas**</span><span class="sxs-lookup"><span data-stu-id="8d7a0-115">&nbsp; &nbsp; **Policy Set**</span></span> | <span data-ttu-id="8d7a0-116">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span><span class="sxs-lookup"><span data-stu-id="8d7a0-116">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span></span>|
|<span data-ttu-id="8d7a0-117">Delegado (conta pessoal da Microsoft)</span><span class="sxs-lookup"><span data-stu-id="8d7a0-117">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="8d7a0-118">Sem suporte.</span><span class="sxs-lookup"><span data-stu-id="8d7a0-118">Not supported.</span></span>|
|<span data-ttu-id="8d7a0-119">Aplicativo</span><span class="sxs-lookup"><span data-stu-id="8d7a0-119">Application</span></span>||
| <span data-ttu-id="8d7a0-120">&nbsp;&nbsp; **Registro**</span><span class="sxs-lookup"><span data-stu-id="8d7a0-120">&nbsp; &nbsp; **Enrollment**</span></span> | <span data-ttu-id="8d7a0-121">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span><span class="sxs-lookup"><span data-stu-id="8d7a0-121">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span></span>|
| <span data-ttu-id="8d7a0-122">&nbsp;&nbsp; **Conjunto de políticas**</span><span class="sxs-lookup"><span data-stu-id="8d7a0-122">&nbsp; &nbsp; **Policy Set**</span></span> | <span data-ttu-id="8d7a0-123">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span><span class="sxs-lookup"><span data-stu-id="8d7a0-123">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span></span>|

## <a name="http-request"></a><span data-ttu-id="8d7a0-124">Solicitação HTTP</span><span class="sxs-lookup"><span data-stu-id="8d7a0-124">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/windowsAutopilotDeploymentProfiles/{windowsAutopilotDeploymentProfileId}
GET /deviceManagement/windowsAutopilotDeviceIdentities/{windowsAutopilotDeviceIdentityId}/deploymentProfile
GET /deviceManagement/windowsAutopilotDeviceIdentities/{windowsAutopilotDeviceIdentityId}/intendedDeploymentProfile
```

## <a name="optional-query-parameters"></a><span data-ttu-id="8d7a0-125">Parâmetros de consulta opcionais</span><span class="sxs-lookup"><span data-stu-id="8d7a0-125">Optional query parameters</span></span>
<span data-ttu-id="8d7a0-126">Este método dá suporte a [Parâmetros de consulta OData](https://docs.microsoft.com/en-us/graph/query-parameters) para ajudar a personalizar a resposta.</span><span class="sxs-lookup"><span data-stu-id="8d7a0-126">This method supports the [OData Query Parameters](https://docs.microsoft.com/en-us/graph/query-parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="8d7a0-127">Cabeçalhos de solicitação</span><span class="sxs-lookup"><span data-stu-id="8d7a0-127">Request headers</span></span>
|<span data-ttu-id="8d7a0-128">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="8d7a0-128">Header</span></span>|<span data-ttu-id="8d7a0-129">Valor</span><span class="sxs-lookup"><span data-stu-id="8d7a0-129">Value</span></span>|
|:---|:---|
|<span data-ttu-id="8d7a0-130">Autorização</span><span class="sxs-lookup"><span data-stu-id="8d7a0-130">Authorization</span></span>|<span data-ttu-id="8d7a0-131">&lt;Token&gt; de portador obrigatório.</span><span class="sxs-lookup"><span data-stu-id="8d7a0-131">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="8d7a0-132">Aceitar</span><span class="sxs-lookup"><span data-stu-id="8d7a0-132">Accept</span></span>|<span data-ttu-id="8d7a0-133">application/json</span><span class="sxs-lookup"><span data-stu-id="8d7a0-133">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="8d7a0-134">Corpo da solicitação</span><span class="sxs-lookup"><span data-stu-id="8d7a0-134">Request body</span></span>
<span data-ttu-id="8d7a0-135">Não forneça um corpo de solicitação para esse método.</span><span class="sxs-lookup"><span data-stu-id="8d7a0-135">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="8d7a0-136">Resposta</span><span class="sxs-lookup"><span data-stu-id="8d7a0-136">Response</span></span>
<span data-ttu-id="8d7a0-137">Se bem-sucedido, este método retorna um `200 OK` código de resposta e um objeto [windowsAutopilotDeploymentProfile](../resources/intune-shared-windowsautopilotdeploymentprofile.md) no corpo da resposta.</span><span class="sxs-lookup"><span data-stu-id="8d7a0-137">If successful, this method returns a `200 OK` response code and [windowsAutopilotDeploymentProfile](../resources/intune-shared-windowsautopilotdeploymentprofile.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="8d7a0-138">Exemplo</span><span class="sxs-lookup"><span data-stu-id="8d7a0-138">Example</span></span>

### <a name="request"></a><span data-ttu-id="8d7a0-139">Solicitação</span><span class="sxs-lookup"><span data-stu-id="8d7a0-139">Request</span></span>
<span data-ttu-id="8d7a0-140">Este é um exemplo da solicitação.</span><span class="sxs-lookup"><span data-stu-id="8d7a0-140">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/windowsAutopilotDeploymentProfiles/{windowsAutopilotDeploymentProfileId}
```

### <a name="response"></a><span data-ttu-id="8d7a0-141">Resposta</span><span class="sxs-lookup"><span data-stu-id="8d7a0-141">Response</span></span>
<span data-ttu-id="8d7a0-p102">Veja a seguir um exemplo da resposta. Observação: o objeto response mostrado aqui pode estar truncado por motivos de concisão. Todas as propriedades serão retornadas de uma chamada real.</span><span class="sxs-lookup"><span data-stu-id="8d7a0-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1409

{
  "value": {
    "@odata.type": "#microsoft.graph.windowsAutopilotDeploymentProfile",
    "id": "9d6394a9-94a9-9d63-a994-639da994639d",
    "displayName": "Display Name value",
    "description": "Description value",
    "language": "Language value",
    "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
    "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
    "outOfBoxExperienceSettings": {
      "@odata.type": "microsoft.graph.outOfBoxExperienceSettings",
      "hidePrivacySettings": true,
      "hideEULA": true,
      "userType": "standard",
      "deviceUsageType": "shared",
      "skipKeyboardSelectionPage": true,
      "hideEscapeLink": true
    },
    "enrollmentStatusScreenSettings": {
      "@odata.type": "microsoft.graph.windowsEnrollmentStatusScreenSettings",
      "hideInstallationProgress": true,
      "allowDeviceUseBeforeProfileAndAppInstallComplete": true,
      "blockDeviceSetupRetryByUser": true,
      "allowLogCollectionOnInstallFailure": true,
      "customErrorMessage": "Custom Error Message value",
      "installProgressTimeoutInMinutes": 15,
      "allowDeviceUseOnInstallFailure": true
    },
    "extractHardwareHash": true,
    "deviceNameTemplate": "Device Name Template value",
    "deviceType": "surfaceHub2",
    "enableWhiteGlove": true,
    "roleScopeTagIds": [
      "Role Scope Tag Ids value"
    ]
  }
}
```



