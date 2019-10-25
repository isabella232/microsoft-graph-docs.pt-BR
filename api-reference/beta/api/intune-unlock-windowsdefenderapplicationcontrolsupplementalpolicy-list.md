---
title: Listar windowsDefenderApplicationControlSupplementalPolicies
description: Listar Propriedades e relações dos objetos windowsDefenderApplicationControlSupplementalPolicy.
author: rolyon
localization_priority: Normal
ms.prod: Intune
doc_type: apiPageType
ms.openlocfilehash: 0d932f7b46d5781b8dfaa3fadd96dc65273f6b2e
ms.sourcegitcommit: 0dcabe677927c259c2ddcefd0d5e2a2aef065e8b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/16/2019
ms.locfileid: "37537668"
---
# <a name="list-windowsdefenderapplicationcontrolsupplementalpolicies"></a><span data-ttu-id="fbf2e-103">Listar windowsDefenderApplicationControlSupplementalPolicies</span><span class="sxs-lookup"><span data-stu-id="fbf2e-103">List windowsDefenderApplicationControlSupplementalPolicies</span></span>

> <span data-ttu-id="fbf2e-104">**Importante:** As APIs do Microsoft Graph na versão/beta estão sujeitas a alterações; Não há suporte para o uso de produção.</span><span class="sxs-lookup"><span data-stu-id="fbf2e-104">**Important:** Microsoft Graph APIs under the /beta version are subject to change; production use is not supported.</span></span>

> <span data-ttu-id="fbf2e-105">**Observação:** A API do Microsoft Graph para Intune requer uma [licença do Active Intune](https://go.microsoft.com/fwlink/?linkid=839381) para o locatário.</span><span class="sxs-lookup"><span data-stu-id="fbf2e-105">**Note:** The Microsoft Graph API for Intune requires an [active Intune license](https://go.microsoft.com/fwlink/?linkid=839381) for the tenant.</span></span>

<span data-ttu-id="fbf2e-106">Listar Propriedades e relações dos objetos [windowsDefenderApplicationControlSupplementalPolicy](../resources/intune-unlock-windowsdefenderapplicationcontrolsupplementalpolicy.md) .</span><span class="sxs-lookup"><span data-stu-id="fbf2e-106">List properties and relationships of the [windowsDefenderApplicationControlSupplementalPolicy](../resources/intune-unlock-windowsdefenderapplicationcontrolsupplementalpolicy.md) objects.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="fbf2e-107">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="fbf2e-107">Prerequisites</span></span>
<span data-ttu-id="fbf2e-p101">Uma das seguintes permissões é obrigatória para chamar esta API. Para saber mais, incluindo como escolher permissões, confira [Permissões](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="fbf2e-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="fbf2e-110">Tipo de permissão</span><span class="sxs-lookup"><span data-stu-id="fbf2e-110">Permission type</span></span>|<span data-ttu-id="fbf2e-111">Permissões (de privilégios máximos a mínimos)</span><span class="sxs-lookup"><span data-stu-id="fbf2e-111">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="fbf2e-112">Delegado (conta corporativa ou de estudante)</span><span class="sxs-lookup"><span data-stu-id="fbf2e-112">Delegated (work or school account)</span></span>|<span data-ttu-id="fbf2e-113">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="fbf2e-113">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="fbf2e-114">Delegado (conta pessoal da Microsoft)</span><span class="sxs-lookup"><span data-stu-id="fbf2e-114">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="fbf2e-115">Sem suporte.</span><span class="sxs-lookup"><span data-stu-id="fbf2e-115">Not supported.</span></span>|
|<span data-ttu-id="fbf2e-116">Application</span><span class="sxs-lookup"><span data-stu-id="fbf2e-116">Application</span></span>|<span data-ttu-id="fbf2e-117">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="fbf2e-117">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|

## <a name="http-request"></a><span data-ttu-id="fbf2e-118">Solicitação HTTP</span><span class="sxs-lookup"><span data-stu-id="fbf2e-118">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/wdacSupplementalPolicies
```

## <a name="request-headers"></a><span data-ttu-id="fbf2e-119">Cabeçalhos de solicitação</span><span class="sxs-lookup"><span data-stu-id="fbf2e-119">Request headers</span></span>
|<span data-ttu-id="fbf2e-120">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="fbf2e-120">Header</span></span>|<span data-ttu-id="fbf2e-121">Valor</span><span class="sxs-lookup"><span data-stu-id="fbf2e-121">Value</span></span>|
|:---|:---|
|<span data-ttu-id="fbf2e-122">Autorização</span><span class="sxs-lookup"><span data-stu-id="fbf2e-122">Authorization</span></span>|<span data-ttu-id="fbf2e-123">&lt;Token&gt; de portador obrigatório.</span><span class="sxs-lookup"><span data-stu-id="fbf2e-123">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="fbf2e-124">Aceitar</span><span class="sxs-lookup"><span data-stu-id="fbf2e-124">Accept</span></span>|<span data-ttu-id="fbf2e-125">application/json</span><span class="sxs-lookup"><span data-stu-id="fbf2e-125">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="fbf2e-126">Corpo da solicitação</span><span class="sxs-lookup"><span data-stu-id="fbf2e-126">Request body</span></span>
<span data-ttu-id="fbf2e-127">Não forneça um corpo de solicitação para esse método.</span><span class="sxs-lookup"><span data-stu-id="fbf2e-127">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="fbf2e-128">Resposta</span><span class="sxs-lookup"><span data-stu-id="fbf2e-128">Response</span></span>
<span data-ttu-id="fbf2e-129">Se tiver êxito, este método retornará `200 OK` um código de resposta e uma coleção de objetos [windowsDefenderApplicationControlSupplementalPolicy](../resources/intune-unlock-windowsdefenderapplicationcontrolsupplementalpolicy.md) no corpo da resposta.</span><span class="sxs-lookup"><span data-stu-id="fbf2e-129">If successful, this method returns a `200 OK` response code and a collection of [windowsDefenderApplicationControlSupplementalPolicy](../resources/intune-unlock-windowsdefenderapplicationcontrolsupplementalpolicy.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="fbf2e-130">Exemplo</span><span class="sxs-lookup"><span data-stu-id="fbf2e-130">Example</span></span>

### <a name="request"></a><span data-ttu-id="fbf2e-131">Solicitação</span><span class="sxs-lookup"><span data-stu-id="fbf2e-131">Request</span></span>
<span data-ttu-id="fbf2e-132">Este é um exemplo da solicitação.</span><span class="sxs-lookup"><span data-stu-id="fbf2e-132">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceAppManagement/wdacSupplementalPolicies
```

### <a name="response"></a><span data-ttu-id="fbf2e-133">Resposta</span><span class="sxs-lookup"><span data-stu-id="fbf2e-133">Response</span></span>
<span data-ttu-id="fbf2e-p102">Veja a seguir um exemplo da resposta. Observação: o objeto response mostrado aqui pode estar truncado por motivos de concisão. Todas as propriedades serão retornadas de uma chamada real.</span><span class="sxs-lookup"><span data-stu-id="fbf2e-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 598

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.windowsDefenderApplicationControlSupplementalPolicy",
      "id": "83d0c39e-c39e-83d0-9ec3-d0839ec3d083",
      "displayName": "Display Name value",
      "description": "Description value",
      "content": "Y29udGVudA==",
      "contentFileName": "Content File Name value",
      "version": "Version value",
      "creationDateTime": "2017-01-01T00:00:43.1365422-08:00",
      "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
      "roleScopeTagIds": [
        "Role Scope Tag Ids value"
      ]
    }
  ]
}
```





