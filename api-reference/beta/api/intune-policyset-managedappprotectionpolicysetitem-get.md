---
title: Obter managedAppProtectionPolicySetItem
description: Leia as propriedades e as relações do objeto managedAppProtectionPolicySetItem.
author: rolyon
localization_priority: Normal
ms.prod: Intune
doc_type: apiPageType
ms.openlocfilehash: 236853d5f2be2a77f7f825244ec216c4a9502db5
ms.sourcegitcommit: 86903a4730bbd825eabb7f0a1b2429723cc8b1e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/26/2019
ms.locfileid: "37191779"
---
# <a name="get-managedappprotectionpolicysetitem"></a><span data-ttu-id="1a224-103">Obter managedAppProtectionPolicySetItem</span><span class="sxs-lookup"><span data-stu-id="1a224-103">Get managedAppProtectionPolicySetItem</span></span>

> <span data-ttu-id="1a224-104">**Importante:** As APIs do Microsoft Graph na versão/beta estão sujeitas a alterações; Não há suporte para o uso de produção.</span><span class="sxs-lookup"><span data-stu-id="1a224-104">**Important:** Microsoft Graph APIs under the /beta version are subject to change; production use is not supported.</span></span>

> <span data-ttu-id="1a224-105">**Observação:** A API do Microsoft Graph para Intune requer uma [licença do Active Intune](https://go.microsoft.com/fwlink/?linkid=839381) para o locatário.</span><span class="sxs-lookup"><span data-stu-id="1a224-105">**Note:** The Microsoft Graph API for Intune requires an [active Intune license](https://go.microsoft.com/fwlink/?linkid=839381) for the tenant.</span></span>

<span data-ttu-id="1a224-106">Leia as propriedades e as relações do objeto [managedAppProtectionPolicySetItem](../resources/intune-policyset-managedappprotectionpolicysetitem.md) .</span><span class="sxs-lookup"><span data-stu-id="1a224-106">Read properties and relationships of the [managedAppProtectionPolicySetItem](../resources/intune-policyset-managedappprotectionpolicysetitem.md) object.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="1a224-107">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="1a224-107">Prerequisites</span></span>
<span data-ttu-id="1a224-p101">Uma das seguintes permissões é obrigatória para chamar esta API. Para saber mais, incluindo como escolher permissões, confira [Permissões](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="1a224-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="1a224-110">Tipo de permissão</span><span class="sxs-lookup"><span data-stu-id="1a224-110">Permission type</span></span>|<span data-ttu-id="1a224-111">Permissões (de privilégios máximos a mínimos)</span><span class="sxs-lookup"><span data-stu-id="1a224-111">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="1a224-112">Delegado (conta corporativa ou de estudante)</span><span class="sxs-lookup"><span data-stu-id="1a224-112">Delegated (work or school account)</span></span>|<span data-ttu-id="1a224-113">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="1a224-113">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="1a224-114">Delegado (conta pessoal da Microsoft)</span><span class="sxs-lookup"><span data-stu-id="1a224-114">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="1a224-115">Sem suporte.</span><span class="sxs-lookup"><span data-stu-id="1a224-115">Not supported.</span></span>|
|<span data-ttu-id="1a224-116">Aplicativo</span><span class="sxs-lookup"><span data-stu-id="1a224-116">Application</span></span>|<span data-ttu-id="1a224-117">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="1a224-117">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|

## <a name="http-request"></a><span data-ttu-id="1a224-118">Solicitação HTTP</span><span class="sxs-lookup"><span data-stu-id="1a224-118">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/policySets/{policySetId}/items/{policySetItemId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="1a224-119">Parâmetros de consulta opcionais</span><span class="sxs-lookup"><span data-stu-id="1a224-119">Optional query parameters</span></span>
<span data-ttu-id="1a224-120">Este método dá suporte a [Parâmetros de consulta OData](https://docs.microsoft.com/en-us/graph/query-parameters) para ajudar a personalizar a resposta.</span><span class="sxs-lookup"><span data-stu-id="1a224-120">This method supports the [OData Query Parameters](https://docs.microsoft.com/en-us/graph/query-parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="1a224-121">Cabeçalhos de solicitação</span><span class="sxs-lookup"><span data-stu-id="1a224-121">Request headers</span></span>
|<span data-ttu-id="1a224-122">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="1a224-122">Header</span></span>|<span data-ttu-id="1a224-123">Valor</span><span class="sxs-lookup"><span data-stu-id="1a224-123">Value</span></span>|
|:---|:---|
|<span data-ttu-id="1a224-124">Autorização</span><span class="sxs-lookup"><span data-stu-id="1a224-124">Authorization</span></span>|<span data-ttu-id="1a224-125">&lt;Token&gt; de portador obrigatório.</span><span class="sxs-lookup"><span data-stu-id="1a224-125">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="1a224-126">Aceitar</span><span class="sxs-lookup"><span data-stu-id="1a224-126">Accept</span></span>|<span data-ttu-id="1a224-127">application/json</span><span class="sxs-lookup"><span data-stu-id="1a224-127">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="1a224-128">Corpo da solicitação</span><span class="sxs-lookup"><span data-stu-id="1a224-128">Request body</span></span>
<span data-ttu-id="1a224-129">Não forneça um corpo de solicitação para esse método.</span><span class="sxs-lookup"><span data-stu-id="1a224-129">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="1a224-130">Resposta</span><span class="sxs-lookup"><span data-stu-id="1a224-130">Response</span></span>
<span data-ttu-id="1a224-131">Se bem-sucedido, este método retorna um `200 OK` código de resposta e um objeto [managedAppProtectionPolicySetItem](../resources/intune-policyset-managedappprotectionpolicysetitem.md) no corpo da resposta.</span><span class="sxs-lookup"><span data-stu-id="1a224-131">If successful, this method returns a `200 OK` response code and [managedAppProtectionPolicySetItem](../resources/intune-policyset-managedappprotectionpolicysetitem.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="1a224-132">Exemplo</span><span class="sxs-lookup"><span data-stu-id="1a224-132">Example</span></span>

### <a name="request"></a><span data-ttu-id="1a224-133">Solicitação</span><span class="sxs-lookup"><span data-stu-id="1a224-133">Request</span></span>
<span data-ttu-id="1a224-134">Este é um exemplo da solicitação.</span><span class="sxs-lookup"><span data-stu-id="1a224-134">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceAppManagement/policySets/{policySetId}/items/{policySetItemId}
```

### <a name="response"></a><span data-ttu-id="1a224-135">Resposta</span><span class="sxs-lookup"><span data-stu-id="1a224-135">Response</span></span>
<span data-ttu-id="1a224-p102">Veja a seguir um exemplo da resposta. Observação: o objeto response mostrado aqui pode estar truncado por motivos de concisão. Todas as propriedades serão retornadas de uma chamada real.</span><span class="sxs-lookup"><span data-stu-id="1a224-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 606

{
  "value": {
    "@odata.type": "#microsoft.graph.managedAppProtectionPolicySetItem",
    "id": "e10d79c9-79c9-e10d-c979-0de1c9790de1",
    "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
    "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
    "payloadId": "Payload Id value",
    "itemType": "Item Type value",
    "displayName": "Display Name value",
    "status": "validating",
    "errorCode": "unauthorized",
    "guidedDeploymentTags": [
      "Guided Deployment Tags value"
    ],
    "targetedAppManagementLevels": "Targeted App Management Levels value"
  }
}
```



