---
title: Obter deviceEnrollmentConfiguration
description: Ler propriedades e relações do objeto deviceEnrollmentConfiguration.
author: rolyon
localization_priority: Normal
ms.prod: Intune
doc_type: apiPageType
ms.openlocfilehash: 0af22a9c351242dba83f397cbcaa36aafe68c0e4
ms.sourcegitcommit: 86903a4730bbd825eabb7f0a1b2429723cc8b1e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/26/2019
ms.locfileid: "37199440"
---
# <a name="get-deviceenrollmentconfiguration"></a><span data-ttu-id="89b1a-103">Obter deviceEnrollmentConfiguration</span><span class="sxs-lookup"><span data-stu-id="89b1a-103">Get deviceEnrollmentConfiguration</span></span>

> <span data-ttu-id="89b1a-104">**Importante:** As APIs do Microsoft Graph na versão/beta estão sujeitas a alterações; Não há suporte para o uso de produção.</span><span class="sxs-lookup"><span data-stu-id="89b1a-104">**Important:** Microsoft Graph APIs under the /beta version are subject to change; production use is not supported.</span></span>

> <span data-ttu-id="89b1a-105">**Observação:** A API do Microsoft Graph para Intune requer uma [licença do Active Intune](https://go.microsoft.com/fwlink/?linkid=839381) para o locatário.</span><span class="sxs-lookup"><span data-stu-id="89b1a-105">**Note:** The Microsoft Graph API for Intune requires an [active Intune license](https://go.microsoft.com/fwlink/?linkid=839381) for the tenant.</span></span>

<span data-ttu-id="89b1a-106">Ler propriedades e relações do objeto [deviceEnrollmentConfiguration](../resources/intune-shared-deviceenrollmentconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="89b1a-106">Read properties and relationships of the [deviceEnrollmentConfiguration](../resources/intune-shared-deviceenrollmentconfiguration.md) object.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="89b1a-107">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="89b1a-107">Prerequisites</span></span>
<span data-ttu-id="89b1a-p101">Uma das seguintes permissões é obrigatória para chamar esta API. Para saber mais, incluindo como escolher permissões, confira [Permissões](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="89b1a-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="89b1a-110">Tipo de permissão</span><span class="sxs-lookup"><span data-stu-id="89b1a-110">Permission type</span></span>|<span data-ttu-id="89b1a-111">Permissões (de privilégios máximos a mínimos)</span><span class="sxs-lookup"><span data-stu-id="89b1a-111">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="89b1a-112">Delegado (conta corporativa ou de estudante)</span><span class="sxs-lookup"><span data-stu-id="89b1a-112">Delegated (work or school account)</span></span>||
| <span data-ttu-id="89b1a-113">&nbsp; &nbsp; **Integração**</span><span class="sxs-lookup"><span data-stu-id="89b1a-113">&nbsp; &nbsp; **Onboarding**</span></span> | <span data-ttu-id="89b1a-114">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span><span class="sxs-lookup"><span data-stu-id="89b1a-114">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span></span>|
| <span data-ttu-id="89b1a-115">&nbsp;&nbsp; **Conjunto de políticas**</span><span class="sxs-lookup"><span data-stu-id="89b1a-115">&nbsp; &nbsp; **Policy Set**</span></span> | <span data-ttu-id="89b1a-116">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span><span class="sxs-lookup"><span data-stu-id="89b1a-116">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span></span>|
|<span data-ttu-id="89b1a-117">Delegado (conta pessoal da Microsoft)</span><span class="sxs-lookup"><span data-stu-id="89b1a-117">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="89b1a-118">Sem suporte.</span><span class="sxs-lookup"><span data-stu-id="89b1a-118">Not supported.</span></span>|
|<span data-ttu-id="89b1a-119">Aplicativo</span><span class="sxs-lookup"><span data-stu-id="89b1a-119">Application</span></span>||
| <span data-ttu-id="89b1a-120">&nbsp; &nbsp; **Integração**</span><span class="sxs-lookup"><span data-stu-id="89b1a-120">&nbsp; &nbsp; **Onboarding**</span></span> | <span data-ttu-id="89b1a-121">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span><span class="sxs-lookup"><span data-stu-id="89b1a-121">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span></span>|
| <span data-ttu-id="89b1a-122">&nbsp;&nbsp; **Conjunto de políticas**</span><span class="sxs-lookup"><span data-stu-id="89b1a-122">&nbsp; &nbsp; **Policy Set**</span></span> | <span data-ttu-id="89b1a-123">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span><span class="sxs-lookup"><span data-stu-id="89b1a-123">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span></span>|

## <a name="http-request"></a><span data-ttu-id="89b1a-124">Solicitação HTTP</span><span class="sxs-lookup"><span data-stu-id="89b1a-124">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceEnrollmentConfigurations/{deviceEnrollmentConfigurationId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="89b1a-125">Parâmetros de consulta opcionais</span><span class="sxs-lookup"><span data-stu-id="89b1a-125">Optional query parameters</span></span>
<span data-ttu-id="89b1a-126">Este método dá suporte a [Parâmetros de consulta OData](https://docs.microsoft.com/en-us/graph/query-parameters) para ajudar a personalizar a resposta.</span><span class="sxs-lookup"><span data-stu-id="89b1a-126">This method supports the [OData Query Parameters](https://docs.microsoft.com/en-us/graph/query-parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="89b1a-127">Cabeçalhos de solicitação</span><span class="sxs-lookup"><span data-stu-id="89b1a-127">Request headers</span></span>
|<span data-ttu-id="89b1a-128">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="89b1a-128">Header</span></span>|<span data-ttu-id="89b1a-129">Valor</span><span class="sxs-lookup"><span data-stu-id="89b1a-129">Value</span></span>|
|:---|:---|
|<span data-ttu-id="89b1a-130">Autorização</span><span class="sxs-lookup"><span data-stu-id="89b1a-130">Authorization</span></span>|<span data-ttu-id="89b1a-131">&lt;Token&gt; de portador obrigatório.</span><span class="sxs-lookup"><span data-stu-id="89b1a-131">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="89b1a-132">Aceitar</span><span class="sxs-lookup"><span data-stu-id="89b1a-132">Accept</span></span>|<span data-ttu-id="89b1a-133">application/json</span><span class="sxs-lookup"><span data-stu-id="89b1a-133">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="89b1a-134">Corpo da solicitação</span><span class="sxs-lookup"><span data-stu-id="89b1a-134">Request body</span></span>
<span data-ttu-id="89b1a-135">Não forneça um corpo de solicitação para esse método.</span><span class="sxs-lookup"><span data-stu-id="89b1a-135">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="89b1a-136">Resposta</span><span class="sxs-lookup"><span data-stu-id="89b1a-136">Response</span></span>
<span data-ttu-id="89b1a-137">Se tiver êxito, este método retornará um código de resposta `200 OK` e um objeto [deviceEnrollmentConfiguration](../resources/intune-shared-deviceenrollmentconfiguration.md) no corpo da resposta.</span><span class="sxs-lookup"><span data-stu-id="89b1a-137">If successful, this method returns a `200 OK` response code and [deviceEnrollmentConfiguration](../resources/intune-shared-deviceenrollmentconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="89b1a-138">Exemplo</span><span class="sxs-lookup"><span data-stu-id="89b1a-138">Example</span></span>

### <a name="request"></a><span data-ttu-id="89b1a-139">Solicitação</span><span class="sxs-lookup"><span data-stu-id="89b1a-139">Request</span></span>
<span data-ttu-id="89b1a-140">Este é um exemplo da solicitação.</span><span class="sxs-lookup"><span data-stu-id="89b1a-140">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/deviceEnrollmentConfigurations/{deviceEnrollmentConfigurationId}
```

### <a name="response"></a><span data-ttu-id="89b1a-141">Resposta</span><span class="sxs-lookup"><span data-stu-id="89b1a-141">Response</span></span>
<span data-ttu-id="89b1a-p102">Veja a seguir um exemplo da resposta. Observação: o objeto response mostrado aqui pode estar truncado por motivos de concisão. Todas as propriedades serão retornadas de uma chamada real.</span><span class="sxs-lookup"><span data-stu-id="89b1a-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 392

{
  "value": {
    "@odata.type": "#microsoft.graph.deviceEnrollmentConfiguration",
    "id": "df13d8b9-d8b9-df13-b9d8-13dfb9d813df",
    "displayName": "Display Name value",
    "description": "Description value",
    "priority": 8,
    "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
    "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
    "version": 7
  }
}
```



