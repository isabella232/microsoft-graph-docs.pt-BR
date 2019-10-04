---
title: Listar deviceEnrollmentConfigurations
description: Listar propriedades e relações de objetos de deviceEnrollmentConfiguration.
author: rolyon
localization_priority: Normal
ms.prod: Intune
doc_type: apiPageType
ms.openlocfilehash: d08ced2b35879cd00d4a4d855638d6bf339cf69a
ms.sourcegitcommit: 86903a4730bbd825eabb7f0a1b2429723cc8b1e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/26/2019
ms.locfileid: "37199437"
---
# <a name="list-deviceenrollmentconfigurations"></a><span data-ttu-id="c7fac-103">Listar deviceEnrollmentConfigurations</span><span class="sxs-lookup"><span data-stu-id="c7fac-103">List deviceEnrollmentConfigurations</span></span>

> <span data-ttu-id="c7fac-104">**Importante:** As APIs do Microsoft Graph na versão/beta estão sujeitas a alterações; Não há suporte para o uso de produção.</span><span class="sxs-lookup"><span data-stu-id="c7fac-104">**Important:** Microsoft Graph APIs under the /beta version are subject to change; production use is not supported.</span></span>

> <span data-ttu-id="c7fac-105">**Observação:** A API do Microsoft Graph para Intune requer uma [licença do Active Intune](https://go.microsoft.com/fwlink/?linkid=839381) para o locatário.</span><span class="sxs-lookup"><span data-stu-id="c7fac-105">**Note:** The Microsoft Graph API for Intune requires an [active Intune license](https://go.microsoft.com/fwlink/?linkid=839381) for the tenant.</span></span>

<span data-ttu-id="c7fac-106">Listar propriedades e relações de objetos de [deviceEnrollmentConfiguration](../resources/intune-shared-deviceenrollmentconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="c7fac-106">List properties and relationships of the [deviceEnrollmentConfiguration](../resources/intune-shared-deviceenrollmentconfiguration.md) objects.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="c7fac-107">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="c7fac-107">Prerequisites</span></span>
<span data-ttu-id="c7fac-p101">Uma das seguintes permissões é obrigatória para chamar esta API. Para saber mais, incluindo como escolher permissões, confira [Permissões](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="c7fac-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="c7fac-110">Tipo de permissão</span><span class="sxs-lookup"><span data-stu-id="c7fac-110">Permission type</span></span>|<span data-ttu-id="c7fac-111">Permissões (de privilégios máximos a mínimos)</span><span class="sxs-lookup"><span data-stu-id="c7fac-111">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="c7fac-112">Delegado (conta corporativa ou de estudante)</span><span class="sxs-lookup"><span data-stu-id="c7fac-112">Delegated (work or school account)</span></span>||
| <span data-ttu-id="c7fac-113">&nbsp; &nbsp; **Integração**</span><span class="sxs-lookup"><span data-stu-id="c7fac-113">&nbsp; &nbsp; **Onboarding**</span></span> | <span data-ttu-id="c7fac-114">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span><span class="sxs-lookup"><span data-stu-id="c7fac-114">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span></span>|
| <span data-ttu-id="c7fac-115">&nbsp;&nbsp; **Conjunto de políticas**</span><span class="sxs-lookup"><span data-stu-id="c7fac-115">&nbsp; &nbsp; **Policy Set**</span></span>| <span data-ttu-id="c7fac-116">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span><span class="sxs-lookup"><span data-stu-id="c7fac-116">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span></span>|
|<span data-ttu-id="c7fac-117">Delegado (conta pessoal da Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c7fac-117">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="c7fac-118">Sem suporte.</span><span class="sxs-lookup"><span data-stu-id="c7fac-118">Not supported.</span></span>|
|<span data-ttu-id="c7fac-119">Aplicativo</span><span class="sxs-lookup"><span data-stu-id="c7fac-119">Application</span></span>||
| <span data-ttu-id="c7fac-120">&nbsp; &nbsp; **Integração**</span><span class="sxs-lookup"><span data-stu-id="c7fac-120">&nbsp; &nbsp; **Onboarding**</span></span> | <span data-ttu-id="c7fac-121">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span><span class="sxs-lookup"><span data-stu-id="c7fac-121">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span></span>|
| <span data-ttu-id="c7fac-122">&nbsp;&nbsp; **Conjunto de políticas**</span><span class="sxs-lookup"><span data-stu-id="c7fac-122">&nbsp; &nbsp; **Policy Set**</span></span> | <span data-ttu-id="c7fac-123">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span><span class="sxs-lookup"><span data-stu-id="c7fac-123">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span></span>|

## <a name="http-request"></a><span data-ttu-id="c7fac-124">Solicitação HTTP</span><span class="sxs-lookup"><span data-stu-id="c7fac-124">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceEnrollmentConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="c7fac-125">Cabeçalhos de solicitação</span><span class="sxs-lookup"><span data-stu-id="c7fac-125">Request headers</span></span>
|<span data-ttu-id="c7fac-126">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="c7fac-126">Header</span></span>|<span data-ttu-id="c7fac-127">Valor</span><span class="sxs-lookup"><span data-stu-id="c7fac-127">Value</span></span>|
|:---|:---|
|<span data-ttu-id="c7fac-128">Autorização</span><span class="sxs-lookup"><span data-stu-id="c7fac-128">Authorization</span></span>|<span data-ttu-id="c7fac-129">&lt;Token&gt; de portador obrigatório.</span><span class="sxs-lookup"><span data-stu-id="c7fac-129">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="c7fac-130">Aceitar</span><span class="sxs-lookup"><span data-stu-id="c7fac-130">Accept</span></span>|<span data-ttu-id="c7fac-131">application/json</span><span class="sxs-lookup"><span data-stu-id="c7fac-131">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="c7fac-132">Corpo da solicitação</span><span class="sxs-lookup"><span data-stu-id="c7fac-132">Request body</span></span>
<span data-ttu-id="c7fac-133">Não forneça um corpo de solicitação para esse método.</span><span class="sxs-lookup"><span data-stu-id="c7fac-133">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="c7fac-134">Resposta</span><span class="sxs-lookup"><span data-stu-id="c7fac-134">Response</span></span>
<span data-ttu-id="c7fac-135">Se tiver êxito, este método retornará um código de resposta `200 OK` e uma coleção de objetos [deviceEnrollmentConfiguration](../resources/intune-shared-deviceenrollmentconfiguration.md) no corpo da resposta.</span><span class="sxs-lookup"><span data-stu-id="c7fac-135">If successful, this method returns a `200 OK` response code and a collection of [deviceEnrollmentConfiguration](../resources/intune-shared-deviceenrollmentconfiguration.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="c7fac-136">Exemplo</span><span class="sxs-lookup"><span data-stu-id="c7fac-136">Example</span></span>

### <a name="request"></a><span data-ttu-id="c7fac-137">Solicitação</span><span class="sxs-lookup"><span data-stu-id="c7fac-137">Request</span></span>
<span data-ttu-id="c7fac-138">Este é um exemplo da solicitação.</span><span class="sxs-lookup"><span data-stu-id="c7fac-138">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/deviceEnrollmentConfigurations
```

### <a name="response"></a><span data-ttu-id="c7fac-139">Resposta</span><span class="sxs-lookup"><span data-stu-id="c7fac-139">Response</span></span>
<span data-ttu-id="c7fac-p102">Veja a seguir um exemplo da resposta. Observação: o objeto response mostrado aqui pode estar truncado por motivos de concisão. Todas as propriedades serão retornadas de uma chamada real.</span><span class="sxs-lookup"><span data-stu-id="c7fac-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 422

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.deviceEnrollmentConfiguration",
      "id": "df13d8b9-d8b9-df13-b9d8-13dfb9d813df",
      "displayName": "Display Name value",
      "description": "Description value",
      "priority": 8,
      "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
      "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
      "version": 7
    }
  ]
}
```



