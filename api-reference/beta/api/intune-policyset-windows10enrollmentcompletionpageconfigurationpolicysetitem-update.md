---
title: Atualizar windows10EnrollmentCompletionPageConfigurationPolicySetItem
description: Atualiza as propriedades de um objeto windows10EnrollmentCompletionPageConfigurationPolicySetItem.
author: rolyon
localization_priority: Normal
ms.prod: Intune
doc_type: apiPageType
ms.openlocfilehash: a5f33cfb3976c66917ecdbdf67146e3d3b02e584
ms.sourcegitcommit: 86903a4730bbd825eabb7f0a1b2429723cc8b1e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/26/2019
ms.locfileid: "37191703"
---
# <a name="update-windows10enrollmentcompletionpageconfigurationpolicysetitem"></a><span data-ttu-id="842af-103">Atualizar windows10EnrollmentCompletionPageConfigurationPolicySetItem</span><span class="sxs-lookup"><span data-stu-id="842af-103">Update windows10EnrollmentCompletionPageConfigurationPolicySetItem</span></span>

> <span data-ttu-id="842af-104">**Importante:** As APIs do Microsoft Graph na versão/beta estão sujeitas a alterações; Não há suporte para o uso de produção.</span><span class="sxs-lookup"><span data-stu-id="842af-104">**Important:** Microsoft Graph APIs under the /beta version are subject to change; production use is not supported.</span></span>

> <span data-ttu-id="842af-105">**Observação:** A API do Microsoft Graph para Intune requer uma [licença do Active Intune](https://go.microsoft.com/fwlink/?linkid=839381) para o locatário.</span><span class="sxs-lookup"><span data-stu-id="842af-105">**Note:** The Microsoft Graph API for Intune requires an [active Intune license](https://go.microsoft.com/fwlink/?linkid=839381) for the tenant.</span></span>

<span data-ttu-id="842af-106">Atualiza as propriedades de um objeto [windows10EnrollmentCompletionPageConfigurationPolicySetItem](../resources/intune-policyset-windows10enrollmentcompletionpageconfigurationpolicysetitem.md) .</span><span class="sxs-lookup"><span data-stu-id="842af-106">Update the properties of a [windows10EnrollmentCompletionPageConfigurationPolicySetItem](../resources/intune-policyset-windows10enrollmentcompletionpageconfigurationpolicysetitem.md) object.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="842af-107">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="842af-107">Prerequisites</span></span>
<span data-ttu-id="842af-p101">Uma das seguintes permissões é obrigatória para chamar esta API. Para saber mais, incluindo como escolher permissões, confira [Permissões](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="842af-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="842af-110">Tipo de permissão</span><span class="sxs-lookup"><span data-stu-id="842af-110">Permission type</span></span>|<span data-ttu-id="842af-111">Permissões (de privilégios máximos a mínimos)</span><span class="sxs-lookup"><span data-stu-id="842af-111">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="842af-112">Delegado (conta corporativa ou de estudante)</span><span class="sxs-lookup"><span data-stu-id="842af-112">Delegated (work or school account)</span></span>|<span data-ttu-id="842af-113">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="842af-113">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="842af-114">Delegado (conta pessoal da Microsoft)</span><span class="sxs-lookup"><span data-stu-id="842af-114">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="842af-115">Sem suporte.</span><span class="sxs-lookup"><span data-stu-id="842af-115">Not supported.</span></span>|
|<span data-ttu-id="842af-116">Aplicativo</span><span class="sxs-lookup"><span data-stu-id="842af-116">Application</span></span>|<span data-ttu-id="842af-117">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="842af-117">DeviceManagementConfiguration.ReadWrite.All</span></span>|

## <a name="http-request"></a><span data-ttu-id="842af-118">Solicitação HTTP</span><span class="sxs-lookup"><span data-stu-id="842af-118">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/policySets/{policySetId}/items/{policySetItemId}
```

## <a name="request-headers"></a><span data-ttu-id="842af-119">Cabeçalhos de solicitação</span><span class="sxs-lookup"><span data-stu-id="842af-119">Request headers</span></span>
|<span data-ttu-id="842af-120">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="842af-120">Header</span></span>|<span data-ttu-id="842af-121">Valor</span><span class="sxs-lookup"><span data-stu-id="842af-121">Value</span></span>|
|:---|:---|
|<span data-ttu-id="842af-122">Autorização</span><span class="sxs-lookup"><span data-stu-id="842af-122">Authorization</span></span>|<span data-ttu-id="842af-123">&lt;Token&gt; de portador obrigatório.</span><span class="sxs-lookup"><span data-stu-id="842af-123">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="842af-124">Aceitar</span><span class="sxs-lookup"><span data-stu-id="842af-124">Accept</span></span>|<span data-ttu-id="842af-125">application/json</span><span class="sxs-lookup"><span data-stu-id="842af-125">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="842af-126">Corpo da solicitação</span><span class="sxs-lookup"><span data-stu-id="842af-126">Request body</span></span>
<span data-ttu-id="842af-127">No corpo da solicitação, forneça uma representação JSON do objeto [windows10EnrollmentCompletionPageConfigurationPolicySetItem](../resources/intune-policyset-windows10enrollmentcompletionpageconfigurationpolicysetitem.md) .</span><span class="sxs-lookup"><span data-stu-id="842af-127">In the request body, supply a JSON representation for the [windows10EnrollmentCompletionPageConfigurationPolicySetItem](../resources/intune-policyset-windows10enrollmentcompletionpageconfigurationpolicysetitem.md) object.</span></span>

<span data-ttu-id="842af-128">A tabela a seguir mostra as propriedades que são necessárias ao criar [windows10EnrollmentCompletionPageConfigurationPolicySetItem](../resources/intune-policyset-windows10enrollmentcompletionpageconfigurationpolicysetitem.md).</span><span class="sxs-lookup"><span data-stu-id="842af-128">The following table shows the properties that are required when you create the [windows10EnrollmentCompletionPageConfigurationPolicySetItem](../resources/intune-policyset-windows10enrollmentcompletionpageconfigurationpolicysetitem.md).</span></span>

|<span data-ttu-id="842af-129">Propriedade</span><span class="sxs-lookup"><span data-stu-id="842af-129">Property</span></span>|<span data-ttu-id="842af-130">Tipo</span><span class="sxs-lookup"><span data-stu-id="842af-130">Type</span></span>|<span data-ttu-id="842af-131">Descrição</span><span class="sxs-lookup"><span data-stu-id="842af-131">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="842af-132">id</span><span class="sxs-lookup"><span data-stu-id="842af-132">id</span></span>|<span data-ttu-id="842af-133">String</span><span class="sxs-lookup"><span data-stu-id="842af-133">String</span></span>|<span data-ttu-id="842af-134">Chave do MobileAppPolicySetItem.</span><span class="sxs-lookup"><span data-stu-id="842af-134">Key of the MobileAppPolicySetItem.</span></span> <span data-ttu-id="842af-135">Herdado de [policySetItem](../resources/intune-policyset-policysetitem.md)</span><span class="sxs-lookup"><span data-stu-id="842af-135">Inherited from [policySetItem](../resources/intune-policyset-policysetitem.md)</span></span>|
|<span data-ttu-id="842af-136">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="842af-136">createdDateTime</span></span>|<span data-ttu-id="842af-137">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="842af-137">DateTimeOffset</span></span>|<span data-ttu-id="842af-138">Hora de criação do PolicySetItem.</span><span class="sxs-lookup"><span data-stu-id="842af-138">Creation time of the PolicySetItem.</span></span> <span data-ttu-id="842af-139">Herdado de [policySetItem](../resources/intune-policyset-policysetitem.md)</span><span class="sxs-lookup"><span data-stu-id="842af-139">Inherited from [policySetItem](../resources/intune-policyset-policysetitem.md)</span></span>|
|<span data-ttu-id="842af-140">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="842af-140">lastModifiedDateTime</span></span>|<span data-ttu-id="842af-141">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="842af-141">DateTimeOffset</span></span>|<span data-ttu-id="842af-142">Hora da última modificação do PolicySetItem.</span><span class="sxs-lookup"><span data-stu-id="842af-142">Last modified time of the PolicySetItem.</span></span> <span data-ttu-id="842af-143">Herdado de [policySetItem](../resources/intune-policyset-policysetitem.md)</span><span class="sxs-lookup"><span data-stu-id="842af-143">Inherited from [policySetItem](../resources/intune-policyset-policysetitem.md)</span></span>|
|<span data-ttu-id="842af-144">payloadId</span><span class="sxs-lookup"><span data-stu-id="842af-144">payloadId</span></span>|<span data-ttu-id="842af-145">String</span><span class="sxs-lookup"><span data-stu-id="842af-145">String</span></span>|<span data-ttu-id="842af-146">PayloadId do PolicySetItem.</span><span class="sxs-lookup"><span data-stu-id="842af-146">PayloadId of the PolicySetItem.</span></span> <span data-ttu-id="842af-147">Herdado de [policySetItem](../resources/intune-policyset-policysetitem.md)</span><span class="sxs-lookup"><span data-stu-id="842af-147">Inherited from [policySetItem](../resources/intune-policyset-policysetitem.md)</span></span>|
|<span data-ttu-id="842af-148">itemType</span><span class="sxs-lookup"><span data-stu-id="842af-148">itemType</span></span>|<span data-ttu-id="842af-149">String</span><span class="sxs-lookup"><span data-stu-id="842af-149">String</span></span>|<span data-ttu-id="842af-150">policySetType do PolicySetItem.</span><span class="sxs-lookup"><span data-stu-id="842af-150">policySetType of the PolicySetItem.</span></span> <span data-ttu-id="842af-151">Herdado de [policySetItem](../resources/intune-policyset-policysetitem.md)</span><span class="sxs-lookup"><span data-stu-id="842af-151">Inherited from [policySetItem](../resources/intune-policyset-policysetitem.md)</span></span>|
|<span data-ttu-id="842af-152">displayName</span><span class="sxs-lookup"><span data-stu-id="842af-152">displayName</span></span>|<span data-ttu-id="842af-153">String</span><span class="sxs-lookup"><span data-stu-id="842af-153">String</span></span>|<span data-ttu-id="842af-154">DisplayName do PolicySetItem.</span><span class="sxs-lookup"><span data-stu-id="842af-154">DisplayName of the PolicySetItem.</span></span> <span data-ttu-id="842af-155">Herdado de [policySetItem](../resources/intune-policyset-policysetitem.md)</span><span class="sxs-lookup"><span data-stu-id="842af-155">Inherited from [policySetItem](../resources/intune-policyset-policysetitem.md)</span></span>|
|<span data-ttu-id="842af-156">status</span><span class="sxs-lookup"><span data-stu-id="842af-156">status</span></span>|[<span data-ttu-id="842af-157">policySetStatus</span><span class="sxs-lookup"><span data-stu-id="842af-157">policySetStatus</span></span>](../resources/intune-policyset-policysetstatus.md)|<span data-ttu-id="842af-158">Status do PolicySetItem.</span><span class="sxs-lookup"><span data-stu-id="842af-158">Status of the PolicySetItem.</span></span> <span data-ttu-id="842af-159">Herdado de [policySetItem](../resources/intune-policyset-policysetitem.md).</span><span class="sxs-lookup"><span data-stu-id="842af-159">Inherited from [policySetItem](../resources/intune-policyset-policysetitem.md).</span></span> <span data-ttu-id="842af-160">Os valores possíveis são: `unknown`, `validating`, `partialSuccess`, `success`, `error`, `notAssigned`.</span><span class="sxs-lookup"><span data-stu-id="842af-160">Possible values are: `unknown`, `validating`, `partialSuccess`, `success`, `error`, `notAssigned`.</span></span>|
|<span data-ttu-id="842af-161">errorCode</span><span class="sxs-lookup"><span data-stu-id="842af-161">errorCode</span></span>|[<span data-ttu-id="842af-162">errorCode</span><span class="sxs-lookup"><span data-stu-id="842af-162">errorCode</span></span>](../resources/intune-policyset-errorcode.md)|<span data-ttu-id="842af-163">Código de erro, caso algum tenha ocorrido.</span><span class="sxs-lookup"><span data-stu-id="842af-163">Error code if any occured.</span></span> <span data-ttu-id="842af-164">Herdado de [policySetItem](../resources/intune-policyset-policysetitem.md).</span><span class="sxs-lookup"><span data-stu-id="842af-164">Inherited from [policySetItem](../resources/intune-policyset-policysetitem.md).</span></span> <span data-ttu-id="842af-165">Os valores possíveis são: `noError`, `unauthorized`, `notFound`, `deleted`.</span><span class="sxs-lookup"><span data-stu-id="842af-165">Possible values are: `noError`, `unauthorized`, `notFound`, `deleted`.</span></span>|
|<span data-ttu-id="842af-166">guidedDeploymentTags</span><span class="sxs-lookup"><span data-stu-id="842af-166">guidedDeploymentTags</span></span>|<span data-ttu-id="842af-167">Coleção de cadeias de caracteres</span><span class="sxs-lookup"><span data-stu-id="842af-167">String collection</span></span>|<span data-ttu-id="842af-168">Marcas da implantação dirigida herdadas de [policySetItem](../resources/intune-policyset-policysetitem.md)</span><span class="sxs-lookup"><span data-stu-id="842af-168">Tags of the guided deployment Inherited from [policySetItem](../resources/intune-policyset-policysetitem.md)</span></span>|
|<span data-ttu-id="842af-169">prioridade</span><span class="sxs-lookup"><span data-stu-id="842af-169">priority</span></span>|<span data-ttu-id="842af-170">Int32</span><span class="sxs-lookup"><span data-stu-id="842af-170">Int32</span></span>|<span data-ttu-id="842af-171">Prioridade do Windows10EnrollmentCompletionPageConfigurationPolicySetItem.</span><span class="sxs-lookup"><span data-stu-id="842af-171">Priority of the Windows10EnrollmentCompletionPageConfigurationPolicySetItem.</span></span>|



## <a name="response"></a><span data-ttu-id="842af-172">Resposta</span><span class="sxs-lookup"><span data-stu-id="842af-172">Response</span></span>
<span data-ttu-id="842af-173">Se tiver êxito, este método retornará `200 OK` um código de resposta e um objeto [windows10EnrollmentCompletionPageConfigurationPolicySetItem](../resources/intune-policyset-windows10enrollmentcompletionpageconfigurationpolicysetitem.md) atualizado no corpo da resposta.</span><span class="sxs-lookup"><span data-stu-id="842af-173">If successful, this method returns a `200 OK` response code and an updated [windows10EnrollmentCompletionPageConfigurationPolicySetItem](../resources/intune-policyset-windows10enrollmentcompletionpageconfigurationpolicysetitem.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="842af-174">Exemplo</span><span class="sxs-lookup"><span data-stu-id="842af-174">Example</span></span>

### <a name="request"></a><span data-ttu-id="842af-175">Solicitação</span><span class="sxs-lookup"><span data-stu-id="842af-175">Request</span></span>
<span data-ttu-id="842af-176">Este é um exemplo da solicitação.</span><span class="sxs-lookup"><span data-stu-id="842af-176">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceAppManagement/policySets/{policySetId}/items/{policySetItemId}
Content-type: application/json
Content-length: 359

{
  "@odata.type": "#microsoft.graph.windows10EnrollmentCompletionPageConfigurationPolicySetItem",
  "payloadId": "Payload Id value",
  "itemType": "Item Type value",
  "displayName": "Display Name value",
  "status": "validating",
  "errorCode": "unauthorized",
  "guidedDeploymentTags": [
    "Guided Deployment Tags value"
  ],
  "priority": 8
}
```

### <a name="response"></a><span data-ttu-id="842af-177">Resposta</span><span class="sxs-lookup"><span data-stu-id="842af-177">Response</span></span>
<span data-ttu-id="842af-p110">Veja a seguir um exemplo da resposta. Observação: o objeto response mostrado aqui pode estar truncado por motivos de concisão. Todas as propriedades serão retornadas de uma chamada real.</span><span class="sxs-lookup"><span data-stu-id="842af-p110">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 531

{
  "@odata.type": "#microsoft.graph.windows10EnrollmentCompletionPageConfigurationPolicySetItem",
  "id": "ebfb1dbb-1dbb-ebfb-bb1d-fbebbb1dfbeb",
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
  "priority": 8
}
```



