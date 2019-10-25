---
title: atribuir ação
description: Ainda não documentado
author: rolyon
localization_priority: Normal
ms.prod: Intune
doc_type: apiPageType
ms.openlocfilehash: 3f0b1c384ba7e868c4f48976144f4413f816404a
ms.sourcegitcommit: 0dcabe677927c259c2ddcefd0d5e2a2aef065e8b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/16/2019
ms.locfileid: "37536697"
---
# <a name="assign-action"></a><span data-ttu-id="63829-103">atribuir ação</span><span class="sxs-lookup"><span data-stu-id="63829-103">assign action</span></span>

> <span data-ttu-id="63829-104">**Importante:** As APIs do Microsoft Graph na versão/beta estão sujeitas a alterações; Não há suporte para o uso de produção.</span><span class="sxs-lookup"><span data-stu-id="63829-104">**Important:** Microsoft Graph APIs under the /beta version are subject to change; production use is not supported.</span></span>

> <span data-ttu-id="63829-105">**Observação:** A API do Microsoft Graph para Intune requer uma [licença do Active Intune](https://go.microsoft.com/fwlink/?linkid=839381) para o locatário.</span><span class="sxs-lookup"><span data-stu-id="63829-105">**Note:** The Microsoft Graph API for Intune requires an [active Intune license](https://go.microsoft.com/fwlink/?linkid=839381) for the tenant.</span></span>

<span data-ttu-id="63829-106">Ainda não documentado</span><span class="sxs-lookup"><span data-stu-id="63829-106">Not yet documented</span></span>

## <a name="prerequisites"></a><span data-ttu-id="63829-107">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="63829-107">Prerequisites</span></span>
<span data-ttu-id="63829-p101">Uma das seguintes permissões é obrigatória para chamar esta API. Para saber mais, incluindo como escolher permissões, confira [Permissões](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="63829-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="63829-110">Tipo de permissão</span><span class="sxs-lookup"><span data-stu-id="63829-110">Permission type</span></span>|<span data-ttu-id="63829-111">Permissões (de privilégios máximos a mínimos)</span><span class="sxs-lookup"><span data-stu-id="63829-111">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="63829-112">Delegado (conta corporativa ou de estudante)</span><span class="sxs-lookup"><span data-stu-id="63829-112">Delegated (work or school account)</span></span>|<span data-ttu-id="63829-113">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="63829-113">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="63829-114">Delegado (conta pessoal da Microsoft)</span><span class="sxs-lookup"><span data-stu-id="63829-114">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="63829-115">Sem suporte.</span><span class="sxs-lookup"><span data-stu-id="63829-115">Not supported.</span></span>|
|<span data-ttu-id="63829-116">Application</span><span class="sxs-lookup"><span data-stu-id="63829-116">Application</span></span>|<span data-ttu-id="63829-117">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="63829-117">DeviceManagementApps.ReadWrite.All</span></span>|

## <a name="http-request"></a><span data-ttu-id="63829-118">Solicitação HTTP</span><span class="sxs-lookup"><span data-stu-id="63829-118">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/wdacSupplementalPolicies/{windowsDefenderApplicationControlSupplementalPolicyId}/assign
POST /deviceAppManagement/wdacSupplementalPolicies/{windowsDefenderApplicationControlSupplementalPolicyId}/deviceStatuses/{windowsDefenderApplicationControlSupplementalPolicyDeploymentStatusId}/policy/assign
```

## <a name="request-headers"></a><span data-ttu-id="63829-119">Cabeçalhos de solicitação</span><span class="sxs-lookup"><span data-stu-id="63829-119">Request headers</span></span>
|<span data-ttu-id="63829-120">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="63829-120">Header</span></span>|<span data-ttu-id="63829-121">Valor</span><span class="sxs-lookup"><span data-stu-id="63829-121">Value</span></span>|
|:---|:---|
|<span data-ttu-id="63829-122">Autorização</span><span class="sxs-lookup"><span data-stu-id="63829-122">Authorization</span></span>|<span data-ttu-id="63829-123">&lt;Token&gt; de portador obrigatório.</span><span class="sxs-lookup"><span data-stu-id="63829-123">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="63829-124">Aceitar</span><span class="sxs-lookup"><span data-stu-id="63829-124">Accept</span></span>|<span data-ttu-id="63829-125">application/json</span><span class="sxs-lookup"><span data-stu-id="63829-125">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="63829-126">Corpo da solicitação</span><span class="sxs-lookup"><span data-stu-id="63829-126">Request body</span></span>
<span data-ttu-id="63829-127">No corpo da solicitação, forneça uma representação JSON dos parâmetros.</span><span class="sxs-lookup"><span data-stu-id="63829-127">In the request body, supply JSON representation of the parameters.</span></span>

<span data-ttu-id="63829-128">A tabela a seguir mostra os parâmetros que podem ser usados com esta ação.</span><span class="sxs-lookup"><span data-stu-id="63829-128">The following table shows the parameters that can be used with this action.</span></span>

|<span data-ttu-id="63829-129">Propriedade</span><span class="sxs-lookup"><span data-stu-id="63829-129">Property</span></span>|<span data-ttu-id="63829-130">Tipo</span><span class="sxs-lookup"><span data-stu-id="63829-130">Type</span></span>|<span data-ttu-id="63829-131">Descrição</span><span class="sxs-lookup"><span data-stu-id="63829-131">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="63829-132">wdacPolicyAssignments</span><span class="sxs-lookup"><span data-stu-id="63829-132">wdacPolicyAssignments</span></span>|<span data-ttu-id="63829-133">coleção [windowsDefenderApplicationControlSupplementalPolicyAssignment](../resources/intune-unlock-windowsdefenderapplicationcontrolsupplementalpolicyassignment.md)</span><span class="sxs-lookup"><span data-stu-id="63829-133">[windowsDefenderApplicationControlSupplementalPolicyAssignment](../resources/intune-unlock-windowsdefenderapplicationcontrolsupplementalpolicyassignment.md) collection</span></span>|<span data-ttu-id="63829-134">Ainda não documentado</span><span class="sxs-lookup"><span data-stu-id="63829-134">Not yet documented</span></span>|



## <a name="response"></a><span data-ttu-id="63829-135">Resposta</span><span class="sxs-lookup"><span data-stu-id="63829-135">Response</span></span>
<span data-ttu-id="63829-136">Se tiver êxito, esta ação retornará um código de resposta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="63829-136">If successful, this action returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="63829-137">Exemplo</span><span class="sxs-lookup"><span data-stu-id="63829-137">Example</span></span>

### <a name="request"></a><span data-ttu-id="63829-138">Solicitação</span><span class="sxs-lookup"><span data-stu-id="63829-138">Request</span></span>
<span data-ttu-id="63829-139">Este é um exemplo da solicitação.</span><span class="sxs-lookup"><span data-stu-id="63829-139">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceAppManagement/wdacSupplementalPolicies/{windowsDefenderApplicationControlSupplementalPolicyId}/assign

Content-type: application/json
Content-length: 319

{
  "wdacPolicyAssignments": [
    {
      "@odata.type": "#microsoft.graph.windowsDefenderApplicationControlSupplementalPolicyAssignment",
      "id": "5e299ff3-9ff3-5e29-f39f-295ef39f295e",
      "target": {
        "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
      }
    }
  ]
}
```

### <a name="response"></a><span data-ttu-id="63829-140">Resposta</span><span class="sxs-lookup"><span data-stu-id="63829-140">Response</span></span>
<span data-ttu-id="63829-p102">Veja a seguir um exemplo da resposta. Observação: o objeto response mostrado aqui pode estar truncado por motivos de concisão. Todas as propriedades serão retornadas de uma chamada real.</span><span class="sxs-lookup"><span data-stu-id="63829-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 204 No Content
```





