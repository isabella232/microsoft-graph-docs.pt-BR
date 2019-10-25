---
title: Criar windowsDefenderApplicationControlSupplementalPolicyAssignment
description: Criar um novo objeto windowsDefenderApplicationControlSupplementalPolicyAssignment.
author: rolyon
localization_priority: Normal
ms.prod: Intune
doc_type: apiPageType
ms.openlocfilehash: db950127a4982033e46d89fe00b08d7d72f1fbb7
ms.sourcegitcommit: 0dcabe677927c259c2ddcefd0d5e2a2aef065e8b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/16/2019
ms.locfileid: "37538249"
---
# <a name="create-windowsdefenderapplicationcontrolsupplementalpolicyassignment"></a><span data-ttu-id="43ef0-103">Criar windowsDefenderApplicationControlSupplementalPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="43ef0-103">Create windowsDefenderApplicationControlSupplementalPolicyAssignment</span></span>

> <span data-ttu-id="43ef0-104">**Importante:** As APIs do Microsoft Graph na versão/beta estão sujeitas a alterações; Não há suporte para o uso de produção.</span><span class="sxs-lookup"><span data-stu-id="43ef0-104">**Important:** Microsoft Graph APIs under the /beta version are subject to change; production use is not supported.</span></span>

> <span data-ttu-id="43ef0-105">**Observação:** A API do Microsoft Graph para Intune requer uma [licença do Active Intune](https://go.microsoft.com/fwlink/?linkid=839381) para o locatário.</span><span class="sxs-lookup"><span data-stu-id="43ef0-105">**Note:** The Microsoft Graph API for Intune requires an [active Intune license](https://go.microsoft.com/fwlink/?linkid=839381) for the tenant.</span></span>

<span data-ttu-id="43ef0-106">Criar um novo objeto [windowsDefenderApplicationControlSupplementalPolicyAssignment](../resources/intune-unlock-windowsdefenderapplicationcontrolsupplementalpolicyassignment.md) .</span><span class="sxs-lookup"><span data-stu-id="43ef0-106">Create a new [windowsDefenderApplicationControlSupplementalPolicyAssignment](../resources/intune-unlock-windowsdefenderapplicationcontrolsupplementalpolicyassignment.md) object.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="43ef0-107">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="43ef0-107">Prerequisites</span></span>
<span data-ttu-id="43ef0-p101">Uma das seguintes permissões é obrigatória para chamar esta API. Para saber mais, incluindo como escolher permissões, confira [Permissões](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="43ef0-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="43ef0-110">Tipo de permissão</span><span class="sxs-lookup"><span data-stu-id="43ef0-110">Permission type</span></span>|<span data-ttu-id="43ef0-111">Permissões (de privilégios máximos a mínimos)</span><span class="sxs-lookup"><span data-stu-id="43ef0-111">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="43ef0-112">Delegado (conta corporativa ou de estudante)</span><span class="sxs-lookup"><span data-stu-id="43ef0-112">Delegated (work or school account)</span></span>|<span data-ttu-id="43ef0-113">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="43ef0-113">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="43ef0-114">Delegado (conta pessoal da Microsoft)</span><span class="sxs-lookup"><span data-stu-id="43ef0-114">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="43ef0-115">Sem suporte.</span><span class="sxs-lookup"><span data-stu-id="43ef0-115">Not supported.</span></span>|
|<span data-ttu-id="43ef0-116">Application</span><span class="sxs-lookup"><span data-stu-id="43ef0-116">Application</span></span>|<span data-ttu-id="43ef0-117">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="43ef0-117">DeviceManagementApps.ReadWrite.All</span></span>|

## <a name="http-request"></a><span data-ttu-id="43ef0-118">Solicitação HTTP</span><span class="sxs-lookup"><span data-stu-id="43ef0-118">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/wdacSupplementalPolicies/{windowsDefenderApplicationControlSupplementalPolicyId}/assignments
```

## <a name="request-headers"></a><span data-ttu-id="43ef0-119">Cabeçalhos de solicitação</span><span class="sxs-lookup"><span data-stu-id="43ef0-119">Request headers</span></span>
|<span data-ttu-id="43ef0-120">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="43ef0-120">Header</span></span>|<span data-ttu-id="43ef0-121">Valor</span><span class="sxs-lookup"><span data-stu-id="43ef0-121">Value</span></span>|
|:---|:---|
|<span data-ttu-id="43ef0-122">Autorização</span><span class="sxs-lookup"><span data-stu-id="43ef0-122">Authorization</span></span>|<span data-ttu-id="43ef0-123">&lt;Token&gt; de portador obrigatório.</span><span class="sxs-lookup"><span data-stu-id="43ef0-123">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="43ef0-124">Aceitar</span><span class="sxs-lookup"><span data-stu-id="43ef0-124">Accept</span></span>|<span data-ttu-id="43ef0-125">application/json</span><span class="sxs-lookup"><span data-stu-id="43ef0-125">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="43ef0-126">Corpo da solicitação</span><span class="sxs-lookup"><span data-stu-id="43ef0-126">Request body</span></span>
<span data-ttu-id="43ef0-127">No corpo da solicitação, forneça uma representação JSON do objeto windowsDefenderApplicationControlSupplementalPolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="43ef0-127">In the request body, supply a JSON representation for the windowsDefenderApplicationControlSupplementalPolicyAssignment object.</span></span>

<span data-ttu-id="43ef0-128">A tabela a seguir mostra as propriedades que são necessárias ao criar windowsDefenderApplicationControlSupplementalPolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="43ef0-128">The following table shows the properties that are required when you create the windowsDefenderApplicationControlSupplementalPolicyAssignment.</span></span>

|<span data-ttu-id="43ef0-129">Propriedade</span><span class="sxs-lookup"><span data-stu-id="43ef0-129">Property</span></span>|<span data-ttu-id="43ef0-130">Tipo</span><span class="sxs-lookup"><span data-stu-id="43ef0-130">Type</span></span>|<span data-ttu-id="43ef0-131">Descrição</span><span class="sxs-lookup"><span data-stu-id="43ef0-131">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="43ef0-132">id</span><span class="sxs-lookup"><span data-stu-id="43ef0-132">id</span></span>|<span data-ttu-id="43ef0-133">Cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="43ef0-133">String</span></span>|<span data-ttu-id="43ef0-134">Chave da entidade.</span><span class="sxs-lookup"><span data-stu-id="43ef0-134">Key of the entity.</span></span>|
|<span data-ttu-id="43ef0-135">destino</span><span class="sxs-lookup"><span data-stu-id="43ef0-135">target</span></span>|[<span data-ttu-id="43ef0-136">deviceAndAppManagementAssignmentTarget</span><span class="sxs-lookup"><span data-stu-id="43ef0-136">deviceAndAppManagementAssignmentTarget</span></span>](../resources/intune-shared-deviceandappmanagementassignmenttarget.md)|<span data-ttu-id="43ef0-137">A atribuição do grupo de destino definida pelo administrador.</span><span class="sxs-lookup"><span data-stu-id="43ef0-137">The target group assignment defined by the admin.</span></span>|



## <a name="response"></a><span data-ttu-id="43ef0-138">Resposta</span><span class="sxs-lookup"><span data-stu-id="43ef0-138">Response</span></span>
<span data-ttu-id="43ef0-139">Se tiver êxito, este método retornará `201 Created` um código de resposta e um objeto [windowsDefenderApplicationControlSupplementalPolicyAssignment](../resources/intune-unlock-windowsdefenderapplicationcontrolsupplementalpolicyassignment.md) no corpo da resposta.</span><span class="sxs-lookup"><span data-stu-id="43ef0-139">If successful, this method returns a `201 Created` response code and a [windowsDefenderApplicationControlSupplementalPolicyAssignment](../resources/intune-unlock-windowsdefenderapplicationcontrolsupplementalpolicyassignment.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="43ef0-140">Exemplo</span><span class="sxs-lookup"><span data-stu-id="43ef0-140">Example</span></span>

### <a name="request"></a><span data-ttu-id="43ef0-141">Solicitação</span><span class="sxs-lookup"><span data-stu-id="43ef0-141">Request</span></span>
<span data-ttu-id="43ef0-142">Este é um exemplo da solicitação.</span><span class="sxs-lookup"><span data-stu-id="43ef0-142">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceAppManagement/wdacSupplementalPolicies/{windowsDefenderApplicationControlSupplementalPolicyId}/assignments
Content-type: application/json
Content-length: 201

{
  "@odata.type": "#microsoft.graph.windowsDefenderApplicationControlSupplementalPolicyAssignment",
  "target": {
    "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
  }
}
```

### <a name="response"></a><span data-ttu-id="43ef0-143">Resposta</span><span class="sxs-lookup"><span data-stu-id="43ef0-143">Response</span></span>
<span data-ttu-id="43ef0-p102">Veja a seguir um exemplo da resposta. Observação: o objeto response mostrado aqui pode estar truncado por motivos de concisão. Todas as propriedades serão retornadas de uma chamada real.</span><span class="sxs-lookup"><span data-stu-id="43ef0-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 250

{
  "@odata.type": "#microsoft.graph.windowsDefenderApplicationControlSupplementalPolicyAssignment",
  "id": "5e299ff3-9ff3-5e29-f39f-295ef39f295e",
  "target": {
    "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
  }
}
```





