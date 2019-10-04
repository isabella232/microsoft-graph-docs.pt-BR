---
title: atribuir ação
description: Ainda não documentado
author: rolyon
localization_priority: Normal
ms.prod: Intune
doc_type: apiPageType
ms.openlocfilehash: 13a2b3f06ce1f02cd68e44257a76b2dc6557f2a0
ms.sourcegitcommit: 86903a4730bbd825eabb7f0a1b2429723cc8b1e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/26/2019
ms.locfileid: "37199430"
---
# <a name="assign-action"></a><span data-ttu-id="608b8-103">atribuir ação</span><span class="sxs-lookup"><span data-stu-id="608b8-103">assign action</span></span>

> <span data-ttu-id="608b8-104">**Importante:** As APIs do Microsoft Graph na versão/beta estão sujeitas a alterações; Não há suporte para o uso de produção.</span><span class="sxs-lookup"><span data-stu-id="608b8-104">**Important:** Microsoft Graph APIs under the /beta version are subject to change; production use is not supported.</span></span>

> <span data-ttu-id="608b8-105">**Observação:** A API do Microsoft Graph para Intune requer uma [licença do Active Intune](https://go.microsoft.com/fwlink/?linkid=839381) para o locatário.</span><span class="sxs-lookup"><span data-stu-id="608b8-105">**Note:** The Microsoft Graph API for Intune requires an [active Intune license](https://go.microsoft.com/fwlink/?linkid=839381) for the tenant.</span></span>

<span data-ttu-id="608b8-106">Ainda não documentado</span><span class="sxs-lookup"><span data-stu-id="608b8-106">Not yet documented</span></span>

## <a name="prerequisites"></a><span data-ttu-id="608b8-107">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="608b8-107">Prerequisites</span></span>
<span data-ttu-id="608b8-p101">Uma das seguintes permissões é obrigatória para chamar esta API. Para saber mais, incluindo como escolher permissões, confira [Permissões](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="608b8-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="608b8-110">Tipo de permissão</span><span class="sxs-lookup"><span data-stu-id="608b8-110">Permission type</span></span>|<span data-ttu-id="608b8-111">Permissões (de privilégios máximos a mínimos)</span><span class="sxs-lookup"><span data-stu-id="608b8-111">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="608b8-112">Delegado (conta corporativa ou de estudante)</span><span class="sxs-lookup"><span data-stu-id="608b8-112">Delegated (work or school account)</span></span>||
| <span data-ttu-id="608b8-113">&nbsp;&nbsp; **Gerenciamento de dispositivos**</span><span class="sxs-lookup"><span data-stu-id="608b8-113">&nbsp; &nbsp; **Device management**</span></span> | <span data-ttu-id="608b8-114">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="608b8-114">DeviceManagementManagedDevices.ReadWrite.All</span></span>|
|<span data-ttu-id="608b8-115">Delegado (conta pessoal da Microsoft)</span><span class="sxs-lookup"><span data-stu-id="608b8-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="608b8-116">Sem suporte.</span><span class="sxs-lookup"><span data-stu-id="608b8-116">Not supported.</span></span>|
|<span data-ttu-id="608b8-117">Aplicativo</span><span class="sxs-lookup"><span data-stu-id="608b8-117">Application</span></span>||
| <span data-ttu-id="608b8-118">&nbsp;&nbsp; **Gerenciamento de dispositivos**</span><span class="sxs-lookup"><span data-stu-id="608b8-118">&nbsp; &nbsp; **Device management**</span></span> | <span data-ttu-id="608b8-119">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="608b8-119">DeviceManagementManagedDevices.ReadWrite.All</span></span>|

## <a name="http-request"></a><span data-ttu-id="608b8-120">Solicitação HTTP</span><span class="sxs-lookup"><span data-stu-id="608b8-120">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceManagementScripts/{deviceManagementScriptId}/assign
```

## <a name="request-headers"></a><span data-ttu-id="608b8-121">Cabeçalhos de solicitação</span><span class="sxs-lookup"><span data-stu-id="608b8-121">Request headers</span></span>
|<span data-ttu-id="608b8-122">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="608b8-122">Header</span></span>|<span data-ttu-id="608b8-123">Valor</span><span class="sxs-lookup"><span data-stu-id="608b8-123">Value</span></span>|
|:---|:---|
|<span data-ttu-id="608b8-124">Autorização</span><span class="sxs-lookup"><span data-stu-id="608b8-124">Authorization</span></span>|<span data-ttu-id="608b8-125">&lt;Token&gt; de portador obrigatório.</span><span class="sxs-lookup"><span data-stu-id="608b8-125">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="608b8-126">Aceitar</span><span class="sxs-lookup"><span data-stu-id="608b8-126">Accept</span></span>|<span data-ttu-id="608b8-127">application/json</span><span class="sxs-lookup"><span data-stu-id="608b8-127">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="608b8-128">Corpo da solicitação</span><span class="sxs-lookup"><span data-stu-id="608b8-128">Request body</span></span>
<span data-ttu-id="608b8-129">No corpo da solicitação, forneça uma representação JSON dos parâmetros.</span><span class="sxs-lookup"><span data-stu-id="608b8-129">In the request body, supply JSON representation of the parameters.</span></span>

<span data-ttu-id="608b8-130">A tabela a seguir mostra os parâmetros que podem ser usados com esta ação.</span><span class="sxs-lookup"><span data-stu-id="608b8-130">The following table shows the parameters that can be used with this action.</span></span>

|<span data-ttu-id="608b8-131">Propriedade</span><span class="sxs-lookup"><span data-stu-id="608b8-131">Property</span></span>|<span data-ttu-id="608b8-132">Tipo</span><span class="sxs-lookup"><span data-stu-id="608b8-132">Type</span></span>|<span data-ttu-id="608b8-133">Descrição</span><span class="sxs-lookup"><span data-stu-id="608b8-133">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="608b8-134">deviceManagementScriptGroupAssignments</span><span class="sxs-lookup"><span data-stu-id="608b8-134">deviceManagementScriptGroupAssignments</span></span>|<span data-ttu-id="608b8-135">coleção [deviceManagementScriptGroupAssignment](../resources/intune-devices-devicemanagementscriptgroupassignment.md)</span><span class="sxs-lookup"><span data-stu-id="608b8-135">[deviceManagementScriptGroupAssignment](../resources/intune-devices-devicemanagementscriptgroupassignment.md) collection</span></span>|<span data-ttu-id="608b8-136">Ainda não documentado</span><span class="sxs-lookup"><span data-stu-id="608b8-136">Not yet documented</span></span>|
|<span data-ttu-id="608b8-137">deviceManagementScriptAssignments</span><span class="sxs-lookup"><span data-stu-id="608b8-137">deviceManagementScriptAssignments</span></span>|<span data-ttu-id="608b8-138">coleção [deviceManagementScriptAssignment](../resources/intune-devices-devicemanagementscriptassignment.md)</span><span class="sxs-lookup"><span data-stu-id="608b8-138">[deviceManagementScriptAssignment](../resources/intune-devices-devicemanagementscriptassignment.md) collection</span></span>|<span data-ttu-id="608b8-139">Ainda não documentado</span><span class="sxs-lookup"><span data-stu-id="608b8-139">Not yet documented</span></span>|



## <a name="response"></a><span data-ttu-id="608b8-140">Resposta</span><span class="sxs-lookup"><span data-stu-id="608b8-140">Response</span></span>
<span data-ttu-id="608b8-141">Se tiver êxito, esta ação retornará um código de resposta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="608b8-141">If successful, this action returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="608b8-142">Exemplo</span><span class="sxs-lookup"><span data-stu-id="608b8-142">Example</span></span>

### <a name="request"></a><span data-ttu-id="608b8-143">Solicitação</span><span class="sxs-lookup"><span data-stu-id="608b8-143">Request</span></span>
<span data-ttu-id="608b8-144">Este é um exemplo da solicitação.</span><span class="sxs-lookup"><span data-stu-id="608b8-144">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/deviceManagementScripts/{deviceManagementScriptId}/assign

Content-type: application/json
Content-length: 550

{
  "deviceManagementScriptGroupAssignments": [
    {
      "@odata.type": "#microsoft.graph.deviceManagementScriptGroupAssignment",
      "id": "ecd2357d-357d-ecd2-7d35-d2ec7d35d2ec",
      "targetGroupId": "Target Group Id value"
    }
  ],
  "deviceManagementScriptAssignments": [
    {
      "@odata.type": "#microsoft.graph.deviceManagementScriptAssignment",
      "id": "a87a601e-601e-a87a-1e60-7aa81e607aa8",
      "target": {
        "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
      }
    }
  ]
}
```

### <a name="response"></a><span data-ttu-id="608b8-145">Resposta</span><span class="sxs-lookup"><span data-stu-id="608b8-145">Response</span></span>
<span data-ttu-id="608b8-p102">Veja a seguir um exemplo da resposta. Observação: o objeto response mostrado aqui pode estar truncado por motivos de concisão. Todas as propriedades serão retornadas de uma chamada real.</span><span class="sxs-lookup"><span data-stu-id="608b8-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 204 No Content
```



