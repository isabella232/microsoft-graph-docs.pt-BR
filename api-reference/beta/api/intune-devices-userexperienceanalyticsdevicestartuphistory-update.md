---
title: Atualizar userExperienceAnalyticsDeviceStartupHistory
description: Atualiza as propriedades de um objeto userExperienceAnalyticsDeviceStartupHistory.
author: rolyon
localization_priority: Normal
ms.prod: Intune
doc_type: apiPageType
ms.openlocfilehash: acf87e008b7e8837da1bd003f183a23c2307d08a
ms.sourcegitcommit: 0dcabe677927c259c2ddcefd0d5e2a2aef065e8b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/16/2019
ms.locfileid: "37529141"
---
# <a name="update-userexperienceanalyticsdevicestartuphistory"></a><span data-ttu-id="be8db-103">Atualizar userExperienceAnalyticsDeviceStartupHistory</span><span class="sxs-lookup"><span data-stu-id="be8db-103">Update userExperienceAnalyticsDeviceStartupHistory</span></span>

> <span data-ttu-id="be8db-104">**Importante:** As APIs do Microsoft Graph na versão/beta estão sujeitas a alterações; Não há suporte para o uso de produção.</span><span class="sxs-lookup"><span data-stu-id="be8db-104">**Important:** Microsoft Graph APIs under the /beta version are subject to change; production use is not supported.</span></span>

> <span data-ttu-id="be8db-105">**Observação:** A API do Microsoft Graph para Intune requer uma [licença do Active Intune](https://go.microsoft.com/fwlink/?linkid=839381) para o locatário.</span><span class="sxs-lookup"><span data-stu-id="be8db-105">**Note:** The Microsoft Graph API for Intune requires an [active Intune license](https://go.microsoft.com/fwlink/?linkid=839381) for the tenant.</span></span>

<span data-ttu-id="be8db-106">Atualiza as propriedades de um objeto [userExperienceAnalyticsDeviceStartupHistory](../resources/intune-devices-userexperienceanalyticsdevicestartuphistory.md) .</span><span class="sxs-lookup"><span data-stu-id="be8db-106">Update the properties of a [userExperienceAnalyticsDeviceStartupHistory](../resources/intune-devices-userexperienceanalyticsdevicestartuphistory.md) object.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="be8db-107">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="be8db-107">Prerequisites</span></span>
<span data-ttu-id="be8db-p101">Uma das seguintes permissões é obrigatória para chamar esta API. Para saber mais, incluindo como escolher permissões, confira [Permissões](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="be8db-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="be8db-110">Tipo de permissão</span><span class="sxs-lookup"><span data-stu-id="be8db-110">Permission type</span></span>|<span data-ttu-id="be8db-111">Permissões (de privilégios máximos a mínimos)</span><span class="sxs-lookup"><span data-stu-id="be8db-111">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="be8db-112">Delegado (conta corporativa ou de estudante)</span><span class="sxs-lookup"><span data-stu-id="be8db-112">Delegated (work or school account)</span></span>|<span data-ttu-id="be8db-113">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="be8db-113">DeviceManagementManagedDevices.ReadWrite.All</span></span>|
|<span data-ttu-id="be8db-114">Delegado (conta pessoal da Microsoft)</span><span class="sxs-lookup"><span data-stu-id="be8db-114">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="be8db-115">Sem suporte.</span><span class="sxs-lookup"><span data-stu-id="be8db-115">Not supported.</span></span>|
|<span data-ttu-id="be8db-116">Application</span><span class="sxs-lookup"><span data-stu-id="be8db-116">Application</span></span>|<span data-ttu-id="be8db-117">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="be8db-117">DeviceManagementManagedDevices.ReadWrite.All</span></span>|

## <a name="http-request"></a><span data-ttu-id="be8db-118">Solicitação HTTP</span><span class="sxs-lookup"><span data-stu-id="be8db-118">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/userExperienceAnalyticsDeviceStartupHistory/{userExperienceAnalyticsDeviceStartupHistoryId}
```

## <a name="request-headers"></a><span data-ttu-id="be8db-119">Cabeçalhos de solicitação</span><span class="sxs-lookup"><span data-stu-id="be8db-119">Request headers</span></span>
|<span data-ttu-id="be8db-120">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="be8db-120">Header</span></span>|<span data-ttu-id="be8db-121">Valor</span><span class="sxs-lookup"><span data-stu-id="be8db-121">Value</span></span>|
|:---|:---|
|<span data-ttu-id="be8db-122">Autorização</span><span class="sxs-lookup"><span data-stu-id="be8db-122">Authorization</span></span>|<span data-ttu-id="be8db-123">&lt;Token&gt; de portador obrigatório.</span><span class="sxs-lookup"><span data-stu-id="be8db-123">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="be8db-124">Aceitar</span><span class="sxs-lookup"><span data-stu-id="be8db-124">Accept</span></span>|<span data-ttu-id="be8db-125">application/json</span><span class="sxs-lookup"><span data-stu-id="be8db-125">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="be8db-126">Corpo da solicitação</span><span class="sxs-lookup"><span data-stu-id="be8db-126">Request body</span></span>
<span data-ttu-id="be8db-127">No corpo da solicitação, forneça uma representação JSON do objeto [userExperienceAnalyticsDeviceStartupHistory](../resources/intune-devices-userexperienceanalyticsdevicestartuphistory.md) .</span><span class="sxs-lookup"><span data-stu-id="be8db-127">In the request body, supply a JSON representation for the [userExperienceAnalyticsDeviceStartupHistory](../resources/intune-devices-userexperienceanalyticsdevicestartuphistory.md) object.</span></span>

<span data-ttu-id="be8db-128">A tabela a seguir mostra as propriedades que são necessárias ao criar [userExperienceAnalyticsDeviceStartupHistory](../resources/intune-devices-userexperienceanalyticsdevicestartuphistory.md).</span><span class="sxs-lookup"><span data-stu-id="be8db-128">The following table shows the properties that are required when you create the [userExperienceAnalyticsDeviceStartupHistory](../resources/intune-devices-userexperienceanalyticsdevicestartuphistory.md).</span></span>

|<span data-ttu-id="be8db-129">Propriedade</span><span class="sxs-lookup"><span data-stu-id="be8db-129">Property</span></span>|<span data-ttu-id="be8db-130">Tipo</span><span class="sxs-lookup"><span data-stu-id="be8db-130">Type</span></span>|<span data-ttu-id="be8db-131">Descrição</span><span class="sxs-lookup"><span data-stu-id="be8db-131">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="be8db-132">id</span><span class="sxs-lookup"><span data-stu-id="be8db-132">id</span></span>|<span data-ttu-id="be8db-133">Cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="be8db-133">String</span></span>|<span data-ttu-id="be8db-134">O identificador exclusivo do histórico de inicialização do dispositivo de análise da experiência do usuário.</span><span class="sxs-lookup"><span data-stu-id="be8db-134">The unique identifier of the user experience analytics device startup history.</span></span>|
|<span data-ttu-id="be8db-135">deviceId</span><span class="sxs-lookup"><span data-stu-id="be8db-135">deviceId</span></span>|<span data-ttu-id="be8db-136">Cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="be8db-136">String</span></span>|<span data-ttu-id="be8db-137">A ID do dispositivo de análise da experiência do usuário.</span><span class="sxs-lookup"><span data-stu-id="be8db-137">The user experience analytics device id.</span></span>|
|<span data-ttu-id="be8db-138">startTime</span><span class="sxs-lookup"><span data-stu-id="be8db-138">startTime</span></span>|<span data-ttu-id="be8db-139">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="be8db-139">DateTimeOffset</span></span>|<span data-ttu-id="be8db-140">A hora de início do dispositivo de análise da experiência do usuário.</span><span class="sxs-lookup"><span data-stu-id="be8db-140">The user experience analytics device boot start time.</span></span>|
|<span data-ttu-id="be8db-141">coreBootTimeInMs</span><span class="sxs-lookup"><span data-stu-id="be8db-141">coreBootTimeInMs</span></span>|<span data-ttu-id="be8db-142">Int32</span><span class="sxs-lookup"><span data-stu-id="be8db-142">Int32</span></span>|<span data-ttu-id="be8db-143">O tempo de inicialização do núcleo do dispositivo de análise da experiência do usuário em milissegundos.</span><span class="sxs-lookup"><span data-stu-id="be8db-143">The user experience analytics device core boot time in milliseconds.</span></span>|
|<span data-ttu-id="be8db-144">groupPolicyBootTimeInMs</span><span class="sxs-lookup"><span data-stu-id="be8db-144">groupPolicyBootTimeInMs</span></span>|<span data-ttu-id="be8db-145">Int32</span><span class="sxs-lookup"><span data-stu-id="be8db-145">Int32</span></span>|<span data-ttu-id="be8db-146">O tempo de inicialização da política de grupo do dispositivo de análise da experiência do usuário em milissegundos.</span><span class="sxs-lookup"><span data-stu-id="be8db-146">The User experience analytics Device group policy boot time in milliseconds.</span></span>|
|<span data-ttu-id="be8db-147">featureUpdateBootTimeInMs</span><span class="sxs-lookup"><span data-stu-id="be8db-147">featureUpdateBootTimeInMs</span></span>|<span data-ttu-id="be8db-148">Int32</span><span class="sxs-lookup"><span data-stu-id="be8db-148">Int32</span></span>|<span data-ttu-id="be8db-149">O tempo de atualização de recursos do dispositivo de análise de experiência do usuário em milissegundos.</span><span class="sxs-lookup"><span data-stu-id="be8db-149">The user experience analytics device feature update time in milliseconds.</span></span>|
|<span data-ttu-id="be8db-150">totalBootTimeInMs</span><span class="sxs-lookup"><span data-stu-id="be8db-150">totalBootTimeInMs</span></span>|<span data-ttu-id="be8db-151">Int32</span><span class="sxs-lookup"><span data-stu-id="be8db-151">Int32</span></span>|<span data-ttu-id="be8db-152">O tempo de inicialização total do dispositivo de análise da experiência do usuário, em milissegundos.</span><span class="sxs-lookup"><span data-stu-id="be8db-152">The user experience analytics device total boot time in milliseconds.</span></span>|
|<span data-ttu-id="be8db-153">groupPolicyLoginTimeInMs</span><span class="sxs-lookup"><span data-stu-id="be8db-153">groupPolicyLoginTimeInMs</span></span>|<span data-ttu-id="be8db-154">Int32</span><span class="sxs-lookup"><span data-stu-id="be8db-154">Int32</span></span>|<span data-ttu-id="be8db-155">O tempo de logon da política de grupo do dispositivo de análise da experiência do usuário em milissegundos.</span><span class="sxs-lookup"><span data-stu-id="be8db-155">The User experience analytics Device group policy login time in milliseconds.</span></span>|
|<span data-ttu-id="be8db-156">coreLoginTimeInMs</span><span class="sxs-lookup"><span data-stu-id="be8db-156">coreLoginTimeInMs</span></span>|<span data-ttu-id="be8db-157">Int32</span><span class="sxs-lookup"><span data-stu-id="be8db-157">Int32</span></span>|<span data-ttu-id="be8db-158">O tempo de logon do dispositivo de análise da experiência do usuário em milissegundos.</span><span class="sxs-lookup"><span data-stu-id="be8db-158">The user experience analytics device core login time in milliseconds.</span></span>|
|<span data-ttu-id="be8db-159">totalLoginTimeInMs</span><span class="sxs-lookup"><span data-stu-id="be8db-159">totalLoginTimeInMs</span></span>|<span data-ttu-id="be8db-160">Int32</span><span class="sxs-lookup"><span data-stu-id="be8db-160">Int32</span></span>|<span data-ttu-id="be8db-161">O tempo total de logon do dispositivo de análise da experiência do usuário em milissegundos.</span><span class="sxs-lookup"><span data-stu-id="be8db-161">The user experience analytics device total login time in milliseconds.</span></span>|
|<span data-ttu-id="be8db-162">isFirstLogin</span><span class="sxs-lookup"><span data-stu-id="be8db-162">isFirstLogin</span></span>|<span data-ttu-id="be8db-163">Booliano</span><span class="sxs-lookup"><span data-stu-id="be8db-163">Boolean</span></span>|<span data-ttu-id="be8db-164">O dispositivo de análise de experiência do usuário primeiro logon.</span><span class="sxs-lookup"><span data-stu-id="be8db-164">The user experience analytics device first login.</span></span>|



## <a name="response"></a><span data-ttu-id="be8db-165">Resposta</span><span class="sxs-lookup"><span data-stu-id="be8db-165">Response</span></span>
<span data-ttu-id="be8db-166">Se tiver êxito, este método retornará `200 OK` um código de resposta e um objeto [userExperienceAnalyticsDeviceStartupHistory](../resources/intune-devices-userexperienceanalyticsdevicestartuphistory.md) atualizado no corpo da resposta.</span><span class="sxs-lookup"><span data-stu-id="be8db-166">If successful, this method returns a `200 OK` response code and an updated [userExperienceAnalyticsDeviceStartupHistory](../resources/intune-devices-userexperienceanalyticsdevicestartuphistory.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="be8db-167">Exemplo</span><span class="sxs-lookup"><span data-stu-id="be8db-167">Example</span></span>

### <a name="request"></a><span data-ttu-id="be8db-168">Solicitação</span><span class="sxs-lookup"><span data-stu-id="be8db-168">Request</span></span>
<span data-ttu-id="be8db-169">Este é um exemplo da solicitação.</span><span class="sxs-lookup"><span data-stu-id="be8db-169">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/userExperienceAnalyticsDeviceStartupHistory/{userExperienceAnalyticsDeviceStartupHistoryId}
Content-type: application/json
Content-length: 407

{
  "@odata.type": "#microsoft.graph.userExperienceAnalyticsDeviceStartupHistory",
  "deviceId": "Device Id value",
  "startTime": "2017-01-01T00:03:29.2730865-08:00",
  "coreBootTimeInMs": 0,
  "groupPolicyBootTimeInMs": 7,
  "featureUpdateBootTimeInMs": 9,
  "totalBootTimeInMs": 1,
  "groupPolicyLoginTimeInMs": 8,
  "coreLoginTimeInMs": 1,
  "totalLoginTimeInMs": 2,
  "isFirstLogin": true
}
```

### <a name="response"></a><span data-ttu-id="be8db-170">Resposta</span><span class="sxs-lookup"><span data-stu-id="be8db-170">Response</span></span>
<span data-ttu-id="be8db-p102">Veja a seguir um exemplo da resposta. Observação: o objeto response mostrado aqui pode estar truncado por motivos de concisão. Todas as propriedades serão retornadas de uma chamada real.</span><span class="sxs-lookup"><span data-stu-id="be8db-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 456

{
  "@odata.type": "#microsoft.graph.userExperienceAnalyticsDeviceStartupHistory",
  "id": "13357123-7123-1335-2371-351323713513",
  "deviceId": "Device Id value",
  "startTime": "2017-01-01T00:03:29.2730865-08:00",
  "coreBootTimeInMs": 0,
  "groupPolicyBootTimeInMs": 7,
  "featureUpdateBootTimeInMs": 9,
  "totalBootTimeInMs": 1,
  "groupPolicyLoginTimeInMs": 8,
  "coreLoginTimeInMs": 1,
  "totalLoginTimeInMs": 2,
  "isFirstLogin": true
}
```





