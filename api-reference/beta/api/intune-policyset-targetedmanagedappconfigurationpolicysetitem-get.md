---
title: Obter targetedManagedAppConfigurationPolicySetItem
description: Leia as propriedades e as relações do objeto targetedManagedAppConfigurationPolicySetItem.
author: rolyon
localization_priority: Normal
ms.prod: Intune
doc_type: apiPageType
ms.openlocfilehash: 75051453404467c5b53f64e39d8d0bc6ba76336c
ms.sourcegitcommit: 86903a4730bbd825eabb7f0a1b2429723cc8b1e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/26/2019
ms.locfileid: "37191716"
---
# <a name="get-targetedmanagedappconfigurationpolicysetitem"></a><span data-ttu-id="096ff-103">Obter targetedManagedAppConfigurationPolicySetItem</span><span class="sxs-lookup"><span data-stu-id="096ff-103">Get targetedManagedAppConfigurationPolicySetItem</span></span>

> <span data-ttu-id="096ff-104">**Importante:** As APIs do Microsoft Graph na versão/beta estão sujeitas a alterações; Não há suporte para o uso de produção.</span><span class="sxs-lookup"><span data-stu-id="096ff-104">**Important:** Microsoft Graph APIs under the /beta version are subject to change; production use is not supported.</span></span>

> <span data-ttu-id="096ff-105">**Observação:** A API do Microsoft Graph para Intune requer uma [licença do Active Intune](https://go.microsoft.com/fwlink/?linkid=839381) para o locatário.</span><span class="sxs-lookup"><span data-stu-id="096ff-105">**Note:** The Microsoft Graph API for Intune requires an [active Intune license](https://go.microsoft.com/fwlink/?linkid=839381) for the tenant.</span></span>

<span data-ttu-id="096ff-106">Leia as propriedades e as relações do objeto [targetedManagedAppConfigurationPolicySetItem](../resources/intune-policyset-targetedmanagedappconfigurationpolicysetitem.md) .</span><span class="sxs-lookup"><span data-stu-id="096ff-106">Read properties and relationships of the [targetedManagedAppConfigurationPolicySetItem](../resources/intune-policyset-targetedmanagedappconfigurationpolicysetitem.md) object.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="096ff-107">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="096ff-107">Prerequisites</span></span>
<span data-ttu-id="096ff-p101">Uma das seguintes permissões é obrigatória para chamar esta API. Para saber mais, incluindo como escolher permissões, confira [Permissões](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="096ff-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="096ff-110">Tipo de permissão</span><span class="sxs-lookup"><span data-stu-id="096ff-110">Permission type</span></span>|<span data-ttu-id="096ff-111">Permissões (de privilégios máximos a mínimos)</span><span class="sxs-lookup"><span data-stu-id="096ff-111">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="096ff-112">Delegado (conta corporativa ou de estudante)</span><span class="sxs-lookup"><span data-stu-id="096ff-112">Delegated (work or school account)</span></span>|<span data-ttu-id="096ff-113">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="096ff-113">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="096ff-114">Delegado (conta pessoal da Microsoft)</span><span class="sxs-lookup"><span data-stu-id="096ff-114">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="096ff-115">Sem suporte.</span><span class="sxs-lookup"><span data-stu-id="096ff-115">Not supported.</span></span>|
|<span data-ttu-id="096ff-116">Aplicativo</span><span class="sxs-lookup"><span data-stu-id="096ff-116">Application</span></span>|<span data-ttu-id="096ff-117">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="096ff-117">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|

## <a name="http-request"></a><span data-ttu-id="096ff-118">Solicitação HTTP</span><span class="sxs-lookup"><span data-stu-id="096ff-118">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/policySets/{policySetId}/items/{policySetItemId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="096ff-119">Parâmetros de consulta opcionais</span><span class="sxs-lookup"><span data-stu-id="096ff-119">Optional query parameters</span></span>
<span data-ttu-id="096ff-120">Este método dá suporte a [Parâmetros de consulta OData](https://docs.microsoft.com/en-us/graph/query-parameters) para ajudar a personalizar a resposta.</span><span class="sxs-lookup"><span data-stu-id="096ff-120">This method supports the [OData Query Parameters](https://docs.microsoft.com/en-us/graph/query-parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="096ff-121">Cabeçalhos de solicitação</span><span class="sxs-lookup"><span data-stu-id="096ff-121">Request headers</span></span>
|<span data-ttu-id="096ff-122">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="096ff-122">Header</span></span>|<span data-ttu-id="096ff-123">Valor</span><span class="sxs-lookup"><span data-stu-id="096ff-123">Value</span></span>|
|:---|:---|
|<span data-ttu-id="096ff-124">Autorização</span><span class="sxs-lookup"><span data-stu-id="096ff-124">Authorization</span></span>|<span data-ttu-id="096ff-125">&lt;Token&gt; de portador obrigatório.</span><span class="sxs-lookup"><span data-stu-id="096ff-125">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="096ff-126">Aceitar</span><span class="sxs-lookup"><span data-stu-id="096ff-126">Accept</span></span>|<span data-ttu-id="096ff-127">application/json</span><span class="sxs-lookup"><span data-stu-id="096ff-127">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="096ff-128">Corpo da solicitação</span><span class="sxs-lookup"><span data-stu-id="096ff-128">Request body</span></span>
<span data-ttu-id="096ff-129">Não forneça um corpo de solicitação para esse método.</span><span class="sxs-lookup"><span data-stu-id="096ff-129">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="096ff-130">Resposta</span><span class="sxs-lookup"><span data-stu-id="096ff-130">Response</span></span>
<span data-ttu-id="096ff-131">Se bem-sucedido, este método retorna um `200 OK` código de resposta e um objeto [targetedManagedAppConfigurationPolicySetItem](../resources/intune-policyset-targetedmanagedappconfigurationpolicysetitem.md) no corpo da resposta.</span><span class="sxs-lookup"><span data-stu-id="096ff-131">If successful, this method returns a `200 OK` response code and [targetedManagedAppConfigurationPolicySetItem](../resources/intune-policyset-targetedmanagedappconfigurationpolicysetitem.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="096ff-132">Exemplo</span><span class="sxs-lookup"><span data-stu-id="096ff-132">Example</span></span>

### <a name="request"></a><span data-ttu-id="096ff-133">Solicitação</span><span class="sxs-lookup"><span data-stu-id="096ff-133">Request</span></span>
<span data-ttu-id="096ff-134">Este é um exemplo da solicitação.</span><span class="sxs-lookup"><span data-stu-id="096ff-134">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceAppManagement/policySets/{policySetId}/items/{policySetItemId}
```

### <a name="response"></a><span data-ttu-id="096ff-135">Resposta</span><span class="sxs-lookup"><span data-stu-id="096ff-135">Response</span></span>
<span data-ttu-id="096ff-p102">Veja a seguir um exemplo da resposta. Observação: o objeto response mostrado aqui pode estar truncado por motivos de concisão. Todas as propriedades serão retornadas de uma chamada real.</span><span class="sxs-lookup"><span data-stu-id="096ff-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 541

{
  "value": {
    "@odata.type": "#microsoft.graph.targetedManagedAppConfigurationPolicySetItem",
    "id": "f86d3112-3112-f86d-1231-6df812316df8",
    "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
    "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
    "payloadId": "Payload Id value",
    "itemType": "Item Type value",
    "displayName": "Display Name value",
    "status": "validating",
    "errorCode": "unauthorized",
    "guidedDeploymentTags": [
      "Guided Deployment Tags value"
    ]
  }
}
```



