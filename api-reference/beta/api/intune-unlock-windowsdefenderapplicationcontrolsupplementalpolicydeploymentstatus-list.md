---
title: Listar windowsDefenderApplicationControlSupplementalPolicyDeploymentStatuses
description: Listar Propriedades e relações dos objetos windowsDefenderApplicationControlSupplementalPolicyDeploymentStatus.
author: rolyon
localization_priority: Normal
ms.prod: Intune
doc_type: apiPageType
ms.openlocfilehash: 1251e33393bef314c8d89f4cb1b7b89f3d7cd74c
ms.sourcegitcommit: 0dcabe677927c259c2ddcefd0d5e2a2aef065e8b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/16/2019
ms.locfileid: "37538235"
---
# <a name="list-windowsdefenderapplicationcontrolsupplementalpolicydeploymentstatuses"></a><span data-ttu-id="19cd0-103">Listar windowsDefenderApplicationControlSupplementalPolicyDeploymentStatuses</span><span class="sxs-lookup"><span data-stu-id="19cd0-103">List windowsDefenderApplicationControlSupplementalPolicyDeploymentStatuses</span></span>

> <span data-ttu-id="19cd0-104">**Importante:** As APIs do Microsoft Graph na versão/beta estão sujeitas a alterações; Não há suporte para o uso de produção.</span><span class="sxs-lookup"><span data-stu-id="19cd0-104">**Important:** Microsoft Graph APIs under the /beta version are subject to change; production use is not supported.</span></span>

> <span data-ttu-id="19cd0-105">**Observação:** A API do Microsoft Graph para Intune requer uma [licença do Active Intune](https://go.microsoft.com/fwlink/?linkid=839381) para o locatário.</span><span class="sxs-lookup"><span data-stu-id="19cd0-105">**Note:** The Microsoft Graph API for Intune requires an [active Intune license](https://go.microsoft.com/fwlink/?linkid=839381) for the tenant.</span></span>

<span data-ttu-id="19cd0-106">Listar Propriedades e relações dos objetos [windowsDefenderApplicationControlSupplementalPolicyDeploymentStatus](../resources/intune-unlock-windowsdefenderapplicationcontrolsupplementalpolicydeploymentstatus.md) .</span><span class="sxs-lookup"><span data-stu-id="19cd0-106">List properties and relationships of the [windowsDefenderApplicationControlSupplementalPolicyDeploymentStatus](../resources/intune-unlock-windowsdefenderapplicationcontrolsupplementalpolicydeploymentstatus.md) objects.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="19cd0-107">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="19cd0-107">Prerequisites</span></span>
<span data-ttu-id="19cd0-p101">Uma das seguintes permissões é obrigatória para chamar esta API. Para saber mais, incluindo como escolher permissões, confira [Permissões](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="19cd0-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="19cd0-110">Tipo de permissão</span><span class="sxs-lookup"><span data-stu-id="19cd0-110">Permission type</span></span>|<span data-ttu-id="19cd0-111">Permissões (de privilégios máximos a mínimos)</span><span class="sxs-lookup"><span data-stu-id="19cd0-111">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="19cd0-112">Delegado (conta corporativa ou de estudante)</span><span class="sxs-lookup"><span data-stu-id="19cd0-112">Delegated (work or school account)</span></span>|<span data-ttu-id="19cd0-113">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="19cd0-113">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="19cd0-114">Delegado (conta pessoal da Microsoft)</span><span class="sxs-lookup"><span data-stu-id="19cd0-114">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="19cd0-115">Sem suporte.</span><span class="sxs-lookup"><span data-stu-id="19cd0-115">Not supported.</span></span>|
|<span data-ttu-id="19cd0-116">Application</span><span class="sxs-lookup"><span data-stu-id="19cd0-116">Application</span></span>|<span data-ttu-id="19cd0-117">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="19cd0-117">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|

## <a name="http-request"></a><span data-ttu-id="19cd0-118">Solicitação HTTP</span><span class="sxs-lookup"><span data-stu-id="19cd0-118">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/wdacSupplementalPolicies/{windowsDefenderApplicationControlSupplementalPolicyId}/deviceStatuses
```

## <a name="request-headers"></a><span data-ttu-id="19cd0-119">Cabeçalhos de solicitação</span><span class="sxs-lookup"><span data-stu-id="19cd0-119">Request headers</span></span>
|<span data-ttu-id="19cd0-120">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="19cd0-120">Header</span></span>|<span data-ttu-id="19cd0-121">Valor</span><span class="sxs-lookup"><span data-stu-id="19cd0-121">Value</span></span>|
|:---|:---|
|<span data-ttu-id="19cd0-122">Autorização</span><span class="sxs-lookup"><span data-stu-id="19cd0-122">Authorization</span></span>|<span data-ttu-id="19cd0-123">&lt;Token&gt; de portador obrigatório.</span><span class="sxs-lookup"><span data-stu-id="19cd0-123">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="19cd0-124">Aceitar</span><span class="sxs-lookup"><span data-stu-id="19cd0-124">Accept</span></span>|<span data-ttu-id="19cd0-125">application/json</span><span class="sxs-lookup"><span data-stu-id="19cd0-125">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="19cd0-126">Corpo da solicitação</span><span class="sxs-lookup"><span data-stu-id="19cd0-126">Request body</span></span>
<span data-ttu-id="19cd0-127">Não forneça um corpo de solicitação para esse método.</span><span class="sxs-lookup"><span data-stu-id="19cd0-127">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="19cd0-128">Resposta</span><span class="sxs-lookup"><span data-stu-id="19cd0-128">Response</span></span>
<span data-ttu-id="19cd0-129">Se tiver êxito, este método retornará `200 OK` um código de resposta e uma coleção de objetos [windowsDefenderApplicationControlSupplementalPolicyDeploymentStatus](../resources/intune-unlock-windowsdefenderapplicationcontrolsupplementalpolicydeploymentstatus.md) no corpo da resposta.</span><span class="sxs-lookup"><span data-stu-id="19cd0-129">If successful, this method returns a `200 OK` response code and a collection of [windowsDefenderApplicationControlSupplementalPolicyDeploymentStatus](../resources/intune-unlock-windowsdefenderapplicationcontrolsupplementalpolicydeploymentstatus.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="19cd0-130">Exemplo</span><span class="sxs-lookup"><span data-stu-id="19cd0-130">Example</span></span>

### <a name="request"></a><span data-ttu-id="19cd0-131">Solicitação</span><span class="sxs-lookup"><span data-stu-id="19cd0-131">Request</span></span>
<span data-ttu-id="19cd0-132">Este é um exemplo da solicitação.</span><span class="sxs-lookup"><span data-stu-id="19cd0-132">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceAppManagement/wdacSupplementalPolicies/{windowsDefenderApplicationControlSupplementalPolicyId}/deviceStatuses
```

### <a name="response"></a><span data-ttu-id="19cd0-133">Resposta</span><span class="sxs-lookup"><span data-stu-id="19cd0-133">Response</span></span>
<span data-ttu-id="19cd0-p102">Veja a seguir um exemplo da resposta. Observação: o objeto response mostrado aqui pode estar truncado por motivos de concisão. Todas as propriedades serão retornadas de uma chamada real.</span><span class="sxs-lookup"><span data-stu-id="19cd0-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 612

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.windowsDefenderApplicationControlSupplementalPolicyDeploymentStatus",
      "id": "e3c01841-1841-e3c0-4118-c0e34118c0e3",
      "deviceName": "Device Name value",
      "deviceId": "Device Id value",
      "lastSyncDateTime": "2017-01-01T00:02:49.3205976-08:00",
      "osVersion": "Os Version value",
      "osDescription": "Os Description value",
      "deploymentStatus": "success",
      "userName": "User Name value",
      "userPrincipalName": "User Principal Name value",
      "policyVersion": "Policy Version value"
    }
  ]
}
```





