---
title: Criar mdmWindowsInformationProtectionPolicyPolicySetItem
description: Criar um novo objeto mdmWindowsInformationProtectionPolicyPolicySetItem.
author: rolyon
localization_priority: Normal
ms.prod: Intune
doc_type: apiPageType
ms.openlocfilehash: 59f87488c032f93e6df8fc34a36219cde3629f5e
ms.sourcegitcommit: 86903a4730bbd825eabb7f0a1b2429723cc8b1e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/26/2019
ms.locfileid: "37191764"
---
# <a name="create-mdmwindowsinformationprotectionpolicypolicysetitem"></a><span data-ttu-id="a71a4-103">Criar mdmWindowsInformationProtectionPolicyPolicySetItem</span><span class="sxs-lookup"><span data-stu-id="a71a4-103">Create mdmWindowsInformationProtectionPolicyPolicySetItem</span></span>

> <span data-ttu-id="a71a4-104">**Importante:** As APIs do Microsoft Graph na versão/beta estão sujeitas a alterações; Não há suporte para o uso de produção.</span><span class="sxs-lookup"><span data-stu-id="a71a4-104">**Important:** Microsoft Graph APIs under the /beta version are subject to change; production use is not supported.</span></span>

> <span data-ttu-id="a71a4-105">**Observação:** A API do Microsoft Graph para Intune requer uma [licença do Active Intune](https://go.microsoft.com/fwlink/?linkid=839381) para o locatário.</span><span class="sxs-lookup"><span data-stu-id="a71a4-105">**Note:** The Microsoft Graph API for Intune requires an [active Intune license](https://go.microsoft.com/fwlink/?linkid=839381) for the tenant.</span></span>

<span data-ttu-id="a71a4-106">Criar um novo objeto [mdmWindowsInformationProtectionPolicyPolicySetItem](../resources/intune-policyset-mdmwindowsinformationprotectionpolicypolicysetitem.md) .</span><span class="sxs-lookup"><span data-stu-id="a71a4-106">Create a new [mdmWindowsInformationProtectionPolicyPolicySetItem](../resources/intune-policyset-mdmwindowsinformationprotectionpolicypolicysetitem.md) object.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="a71a4-107">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="a71a4-107">Prerequisites</span></span>
<span data-ttu-id="a71a4-p101">Uma das seguintes permissões é obrigatória para chamar esta API. Para saber mais, incluindo como escolher permissões, confira [Permissões](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a71a4-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="a71a4-110">Tipo de permissão</span><span class="sxs-lookup"><span data-stu-id="a71a4-110">Permission type</span></span>|<span data-ttu-id="a71a4-111">Permissões (de privilégios máximos a mínimos)</span><span class="sxs-lookup"><span data-stu-id="a71a4-111">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="a71a4-112">Delegado (conta corporativa ou de estudante)</span><span class="sxs-lookup"><span data-stu-id="a71a4-112">Delegated (work or school account)</span></span>|<span data-ttu-id="a71a4-113">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="a71a4-113">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="a71a4-114">Delegado (conta pessoal da Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a71a4-114">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="a71a4-115">Sem suporte.</span><span class="sxs-lookup"><span data-stu-id="a71a4-115">Not supported.</span></span>|
|<span data-ttu-id="a71a4-116">Aplicativo</span><span class="sxs-lookup"><span data-stu-id="a71a4-116">Application</span></span>|<span data-ttu-id="a71a4-117">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="a71a4-117">DeviceManagementConfiguration.ReadWrite.All</span></span>|

## <a name="http-request"></a><span data-ttu-id="a71a4-118">Solicitação HTTP</span><span class="sxs-lookup"><span data-stu-id="a71a4-118">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/policySets/{policySetId}/items
```

## <a name="request-headers"></a><span data-ttu-id="a71a4-119">Cabeçalhos de solicitação</span><span class="sxs-lookup"><span data-stu-id="a71a4-119">Request headers</span></span>
|<span data-ttu-id="a71a4-120">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="a71a4-120">Header</span></span>|<span data-ttu-id="a71a4-121">Valor</span><span class="sxs-lookup"><span data-stu-id="a71a4-121">Value</span></span>|
|:---|:---|
|<span data-ttu-id="a71a4-122">Autorização</span><span class="sxs-lookup"><span data-stu-id="a71a4-122">Authorization</span></span>|<span data-ttu-id="a71a4-123">&lt;Token&gt; de portador obrigatório.</span><span class="sxs-lookup"><span data-stu-id="a71a4-123">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="a71a4-124">Aceitar</span><span class="sxs-lookup"><span data-stu-id="a71a4-124">Accept</span></span>|<span data-ttu-id="a71a4-125">application/json</span><span class="sxs-lookup"><span data-stu-id="a71a4-125">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="a71a4-126">Corpo da solicitação</span><span class="sxs-lookup"><span data-stu-id="a71a4-126">Request body</span></span>
<span data-ttu-id="a71a4-127">No corpo da solicitação, forneça uma representação JSON do objeto mdmWindowsInformationProtectionPolicyPolicySetItem.</span><span class="sxs-lookup"><span data-stu-id="a71a4-127">In the request body, supply a JSON representation for the mdmWindowsInformationProtectionPolicyPolicySetItem object.</span></span>

<span data-ttu-id="a71a4-128">A tabela a seguir mostra as propriedades que são necessárias ao criar mdmWindowsInformationProtectionPolicyPolicySetItem.</span><span class="sxs-lookup"><span data-stu-id="a71a4-128">The following table shows the properties that are required when you create the mdmWindowsInformationProtectionPolicyPolicySetItem.</span></span>

|<span data-ttu-id="a71a4-129">Propriedade</span><span class="sxs-lookup"><span data-stu-id="a71a4-129">Property</span></span>|<span data-ttu-id="a71a4-130">Tipo</span><span class="sxs-lookup"><span data-stu-id="a71a4-130">Type</span></span>|<span data-ttu-id="a71a4-131">Descrição</span><span class="sxs-lookup"><span data-stu-id="a71a4-131">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="a71a4-132">id</span><span class="sxs-lookup"><span data-stu-id="a71a4-132">id</span></span>|<span data-ttu-id="a71a4-133">String</span><span class="sxs-lookup"><span data-stu-id="a71a4-133">String</span></span>|<span data-ttu-id="a71a4-134">Chave do MobileAppPolicySetItem.</span><span class="sxs-lookup"><span data-stu-id="a71a4-134">Key of the MobileAppPolicySetItem.</span></span> <span data-ttu-id="a71a4-135">Herdado de [policySetItem](../resources/intune-policyset-policysetitem.md)</span><span class="sxs-lookup"><span data-stu-id="a71a4-135">Inherited from [policySetItem](../resources/intune-policyset-policysetitem.md)</span></span>|
|<span data-ttu-id="a71a4-136">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="a71a4-136">createdDateTime</span></span>|<span data-ttu-id="a71a4-137">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="a71a4-137">DateTimeOffset</span></span>|<span data-ttu-id="a71a4-138">Hora de criação do PolicySetItem.</span><span class="sxs-lookup"><span data-stu-id="a71a4-138">Creation time of the PolicySetItem.</span></span> <span data-ttu-id="a71a4-139">Herdado de [policySetItem](../resources/intune-policyset-policysetitem.md)</span><span class="sxs-lookup"><span data-stu-id="a71a4-139">Inherited from [policySetItem](../resources/intune-policyset-policysetitem.md)</span></span>|
|<span data-ttu-id="a71a4-140">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="a71a4-140">lastModifiedDateTime</span></span>|<span data-ttu-id="a71a4-141">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="a71a4-141">DateTimeOffset</span></span>|<span data-ttu-id="a71a4-142">Hora da última modificação do PolicySetItem.</span><span class="sxs-lookup"><span data-stu-id="a71a4-142">Last modified time of the PolicySetItem.</span></span> <span data-ttu-id="a71a4-143">Herdado de [policySetItem](../resources/intune-policyset-policysetitem.md)</span><span class="sxs-lookup"><span data-stu-id="a71a4-143">Inherited from [policySetItem](../resources/intune-policyset-policysetitem.md)</span></span>|
|<span data-ttu-id="a71a4-144">payloadId</span><span class="sxs-lookup"><span data-stu-id="a71a4-144">payloadId</span></span>|<span data-ttu-id="a71a4-145">String</span><span class="sxs-lookup"><span data-stu-id="a71a4-145">String</span></span>|<span data-ttu-id="a71a4-146">PayloadId do PolicySetItem.</span><span class="sxs-lookup"><span data-stu-id="a71a4-146">PayloadId of the PolicySetItem.</span></span> <span data-ttu-id="a71a4-147">Herdado de [policySetItem](../resources/intune-policyset-policysetitem.md)</span><span class="sxs-lookup"><span data-stu-id="a71a4-147">Inherited from [policySetItem](../resources/intune-policyset-policysetitem.md)</span></span>|
|<span data-ttu-id="a71a4-148">itemType</span><span class="sxs-lookup"><span data-stu-id="a71a4-148">itemType</span></span>|<span data-ttu-id="a71a4-149">String</span><span class="sxs-lookup"><span data-stu-id="a71a4-149">String</span></span>|<span data-ttu-id="a71a4-150">policySetType do PolicySetItem.</span><span class="sxs-lookup"><span data-stu-id="a71a4-150">policySetType of the PolicySetItem.</span></span> <span data-ttu-id="a71a4-151">Herdado de [policySetItem](../resources/intune-policyset-policysetitem.md)</span><span class="sxs-lookup"><span data-stu-id="a71a4-151">Inherited from [policySetItem](../resources/intune-policyset-policysetitem.md)</span></span>|
|<span data-ttu-id="a71a4-152">displayName</span><span class="sxs-lookup"><span data-stu-id="a71a4-152">displayName</span></span>|<span data-ttu-id="a71a4-153">String</span><span class="sxs-lookup"><span data-stu-id="a71a4-153">String</span></span>|<span data-ttu-id="a71a4-154">DisplayName do PolicySetItem.</span><span class="sxs-lookup"><span data-stu-id="a71a4-154">DisplayName of the PolicySetItem.</span></span> <span data-ttu-id="a71a4-155">Herdado de [policySetItem](../resources/intune-policyset-policysetitem.md)</span><span class="sxs-lookup"><span data-stu-id="a71a4-155">Inherited from [policySetItem](../resources/intune-policyset-policysetitem.md)</span></span>|
|<span data-ttu-id="a71a4-156">status</span><span class="sxs-lookup"><span data-stu-id="a71a4-156">status</span></span>|[<span data-ttu-id="a71a4-157">policySetStatus</span><span class="sxs-lookup"><span data-stu-id="a71a4-157">policySetStatus</span></span>](../resources/intune-policyset-policysetstatus.md)|<span data-ttu-id="a71a4-158">Status do PolicySetItem.</span><span class="sxs-lookup"><span data-stu-id="a71a4-158">Status of the PolicySetItem.</span></span> <span data-ttu-id="a71a4-159">Herdado de [policySetItem](../resources/intune-policyset-policysetitem.md).</span><span class="sxs-lookup"><span data-stu-id="a71a4-159">Inherited from [policySetItem](../resources/intune-policyset-policysetitem.md).</span></span> <span data-ttu-id="a71a4-160">Os valores possíveis são: `unknown`, `validating`, `partialSuccess`, `success`, `error`, `notAssigned`.</span><span class="sxs-lookup"><span data-stu-id="a71a4-160">Possible values are: `unknown`, `validating`, `partialSuccess`, `success`, `error`, `notAssigned`.</span></span>|
|<span data-ttu-id="a71a4-161">errorCode</span><span class="sxs-lookup"><span data-stu-id="a71a4-161">errorCode</span></span>|[<span data-ttu-id="a71a4-162">errorCode</span><span class="sxs-lookup"><span data-stu-id="a71a4-162">errorCode</span></span>](../resources/intune-policyset-errorcode.md)|<span data-ttu-id="a71a4-163">Código de erro, caso algum tenha ocorrido.</span><span class="sxs-lookup"><span data-stu-id="a71a4-163">Error code if any occured.</span></span> <span data-ttu-id="a71a4-164">Herdado de [policySetItem](../resources/intune-policyset-policysetitem.md).</span><span class="sxs-lookup"><span data-stu-id="a71a4-164">Inherited from [policySetItem](../resources/intune-policyset-policysetitem.md).</span></span> <span data-ttu-id="a71a4-165">Os valores possíveis são: `noError`, `unauthorized`, `notFound`, `deleted`.</span><span class="sxs-lookup"><span data-stu-id="a71a4-165">Possible values are: `noError`, `unauthorized`, `notFound`, `deleted`.</span></span>|
|<span data-ttu-id="a71a4-166">guidedDeploymentTags</span><span class="sxs-lookup"><span data-stu-id="a71a4-166">guidedDeploymentTags</span></span>|<span data-ttu-id="a71a4-167">Coleção de cadeias de caracteres</span><span class="sxs-lookup"><span data-stu-id="a71a4-167">String collection</span></span>|<span data-ttu-id="a71a4-168">Marcas da implantação dirigida herdadas de [policySetItem](../resources/intune-policyset-policysetitem.md)</span><span class="sxs-lookup"><span data-stu-id="a71a4-168">Tags of the guided deployment Inherited from [policySetItem](../resources/intune-policyset-policysetitem.md)</span></span>|



## <a name="response"></a><span data-ttu-id="a71a4-169">Resposta</span><span class="sxs-lookup"><span data-stu-id="a71a4-169">Response</span></span>
<span data-ttu-id="a71a4-170">Se tiver êxito, este método retornará `201 Created` um código de resposta e um objeto [mdmWindowsInformationProtectionPolicyPolicySetItem](../resources/intune-policyset-mdmwindowsinformationprotectionpolicypolicysetitem.md) no corpo da resposta.</span><span class="sxs-lookup"><span data-stu-id="a71a4-170">If successful, this method returns a `201 Created` response code and a [mdmWindowsInformationProtectionPolicyPolicySetItem](../resources/intune-policyset-mdmwindowsinformationprotectionpolicypolicysetitem.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="a71a4-171">Exemplo</span><span class="sxs-lookup"><span data-stu-id="a71a4-171">Example</span></span>

### <a name="request"></a><span data-ttu-id="a71a4-172">Solicitação</span><span class="sxs-lookup"><span data-stu-id="a71a4-172">Request</span></span>
<span data-ttu-id="a71a4-173">Este é um exemplo da solicitação.</span><span class="sxs-lookup"><span data-stu-id="a71a4-173">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceAppManagement/policySets/{policySetId}/items
Content-type: application/json
Content-length: 332

{
  "@odata.type": "#microsoft.graph.mdmWindowsInformationProtectionPolicyPolicySetItem",
  "payloadId": "Payload Id value",
  "itemType": "Item Type value",
  "displayName": "Display Name value",
  "status": "validating",
  "errorCode": "unauthorized",
  "guidedDeploymentTags": [
    "Guided Deployment Tags value"
  ]
}
```

### <a name="response"></a><span data-ttu-id="a71a4-174">Resposta</span><span class="sxs-lookup"><span data-stu-id="a71a4-174">Response</span></span>
<span data-ttu-id="a71a4-p110">Veja a seguir um exemplo da resposta. Observação: o objeto response mostrado aqui pode estar truncado por motivos de concisão. Todas as propriedades serão retornadas de uma chamada real.</span><span class="sxs-lookup"><span data-stu-id="a71a4-p110">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 504

{
  "@odata.type": "#microsoft.graph.mdmWindowsInformationProtectionPolicyPolicySetItem",
  "id": "4ac5be70-be70-4ac5-70be-c54a70bec54a",
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
```



