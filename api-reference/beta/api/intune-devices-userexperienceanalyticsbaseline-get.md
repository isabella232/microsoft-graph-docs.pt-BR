---
title: Obter userExperienceAnalyticsBaseline
description: Leia as propriedades e as relações do objeto userExperienceAnalyticsBaseline.
author: rolyon
localization_priority: Normal
ms.prod: Intune
doc_type: apiPageType
ms.openlocfilehash: b712fc30400212d1330b024040faab1163523b24
ms.sourcegitcommit: b5425ebf648572569b032ded5b56e1dcf3830515
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/13/2019
ms.locfileid: "36350424"
---
# <a name="get-userexperienceanalyticsbaseline"></a><span data-ttu-id="a914d-103">Obter userExperienceAnalyticsBaseline</span><span class="sxs-lookup"><span data-stu-id="a914d-103">Get userExperienceAnalyticsBaseline</span></span>

> <span data-ttu-id="a914d-104">**Importante:** As APIs do Microsoft Graph na versão/beta estão sujeitas a alterações; Não há suporte para o uso de produção.</span><span class="sxs-lookup"><span data-stu-id="a914d-104">**Important:** Microsoft Graph APIs under the /beta version are subject to change; production use is not supported.</span></span>

> <span data-ttu-id="a914d-105">**Observação:** A API do Microsoft Graph para Intune requer uma [licença do Active Intune](https://go.microsoft.com/fwlink/?linkid=839381) para o locatário.</span><span class="sxs-lookup"><span data-stu-id="a914d-105">**Note:** The Microsoft Graph API for Intune requires an [active Intune license](https://go.microsoft.com/fwlink/?linkid=839381) for the tenant.</span></span>

<span data-ttu-id="a914d-106">Leia as propriedades e as relações do objeto [userExperienceAnalyticsBaseline](../resources/intune-devices-userexperienceanalyticsbaseline.md) .</span><span class="sxs-lookup"><span data-stu-id="a914d-106">Read properties and relationships of the [userExperienceAnalyticsBaseline](../resources/intune-devices-userexperienceanalyticsbaseline.md) object.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="a914d-107">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="a914d-107">Prerequisites</span></span>
<span data-ttu-id="a914d-p101">Uma das seguintes permissões é obrigatória para chamar esta API. Para saber mais, incluindo como escolher permissões, confira [Permissões](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a914d-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="a914d-110">Tipo de permissão</span><span class="sxs-lookup"><span data-stu-id="a914d-110">Permission type</span></span>|<span data-ttu-id="a914d-111">Permissões (de privilégios máximos a mínimos)</span><span class="sxs-lookup"><span data-stu-id="a914d-111">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="a914d-112">Delegado (conta corporativa ou de estudante)</span><span class="sxs-lookup"><span data-stu-id="a914d-112">Delegated (work or school account)</span></span>|<span data-ttu-id="a914d-113">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span><span class="sxs-lookup"><span data-stu-id="a914d-113">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span></span>|
|<span data-ttu-id="a914d-114">Delegado (conta pessoal da Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a914d-114">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="a914d-115">Sem suporte.</span><span class="sxs-lookup"><span data-stu-id="a914d-115">Not supported.</span></span>|
|<span data-ttu-id="a914d-116">Aplicativo</span><span class="sxs-lookup"><span data-stu-id="a914d-116">Application</span></span>|<span data-ttu-id="a914d-117">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span><span class="sxs-lookup"><span data-stu-id="a914d-117">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span></span>|

## <a name="http-request"></a><span data-ttu-id="a914d-118">Solicitação HTTP</span><span class="sxs-lookup"><span data-stu-id="a914d-118">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/userExperienceAnalyticsBaselines/{userExperienceAnalyticsBaselineId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="a914d-119">Parâmetros de consulta opcionais</span><span class="sxs-lookup"><span data-stu-id="a914d-119">Optional query parameters</span></span>
<span data-ttu-id="a914d-120">Este método dá suporte a [Parâmetros de consulta OData](https://docs.microsoft.com/en-us/graph/query-parameters) para ajudar a personalizar a resposta.</span><span class="sxs-lookup"><span data-stu-id="a914d-120">This method supports the [OData Query Parameters](https://docs.microsoft.com/en-us/graph/query-parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="a914d-121">Cabeçalhos de solicitação</span><span class="sxs-lookup"><span data-stu-id="a914d-121">Request headers</span></span>
|<span data-ttu-id="a914d-122">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="a914d-122">Header</span></span>|<span data-ttu-id="a914d-123">Valor</span><span class="sxs-lookup"><span data-stu-id="a914d-123">Value</span></span>|
|:---|:---|
|<span data-ttu-id="a914d-124">Autorização</span><span class="sxs-lookup"><span data-stu-id="a914d-124">Authorization</span></span>|<span data-ttu-id="a914d-125">&lt;Token&gt; de portador obrigatório.</span><span class="sxs-lookup"><span data-stu-id="a914d-125">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="a914d-126">Aceitar</span><span class="sxs-lookup"><span data-stu-id="a914d-126">Accept</span></span>|<span data-ttu-id="a914d-127">application/json</span><span class="sxs-lookup"><span data-stu-id="a914d-127">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="a914d-128">Corpo da solicitação</span><span class="sxs-lookup"><span data-stu-id="a914d-128">Request body</span></span>
<span data-ttu-id="a914d-129">Não forneça um corpo de solicitação para esse método.</span><span class="sxs-lookup"><span data-stu-id="a914d-129">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="a914d-130">Resposta</span><span class="sxs-lookup"><span data-stu-id="a914d-130">Response</span></span>
<span data-ttu-id="a914d-131">Se bem-sucedido, este método retorna um `200 OK` código de resposta e um objeto [userExperienceAnalyticsBaseline](../resources/intune-devices-userexperienceanalyticsbaseline.md) no corpo da resposta.</span><span class="sxs-lookup"><span data-stu-id="a914d-131">If successful, this method returns a `200 OK` response code and [userExperienceAnalyticsBaseline](../resources/intune-devices-userexperienceanalyticsbaseline.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="a914d-132">Exemplo</span><span class="sxs-lookup"><span data-stu-id="a914d-132">Example</span></span>

### <a name="request"></a><span data-ttu-id="a914d-133">Solicitação</span><span class="sxs-lookup"><span data-stu-id="a914d-133">Request</span></span>
<span data-ttu-id="a914d-134">Este é um exemplo da solicitação.</span><span class="sxs-lookup"><span data-stu-id="a914d-134">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/userExperienceAnalyticsBaselines/{userExperienceAnalyticsBaselineId}
```

### <a name="response"></a><span data-ttu-id="a914d-135">Resposta</span><span class="sxs-lookup"><span data-stu-id="a914d-135">Response</span></span>
<span data-ttu-id="a914d-p102">Veja a seguir um exemplo da resposta. Observação: o objeto response mostrado aqui pode estar truncado por motivos de concisão. Todas as propriedades serão retornadas de uma chamada real.</span><span class="sxs-lookup"><span data-stu-id="a914d-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 251

{
  "value": {
    "@odata.type": "#microsoft.graph.userExperienceAnalyticsBaseline",
    "id": "1cce2cab-2cab-1cce-ab2c-ce1cab2cce1c",
    "displayName": "Display Name value",
    "overallScore": 12,
    "overallRegressionThreshold": 10
  }
}
```





