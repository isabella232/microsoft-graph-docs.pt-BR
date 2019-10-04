---
title: Criar policyset
description: Criar um novo objeto policyset.
author: rolyon
localization_priority: Normal
ms.prod: Intune
doc_type: apiPageType
ms.openlocfilehash: 9774bb5f81f7d114b5f1ff1031138f922460027e
ms.sourcegitcommit: 86903a4730bbd825eabb7f0a1b2429723cc8b1e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/26/2019
ms.locfileid: "37191743"
---
# <a name="create-policyset"></a><span data-ttu-id="83f66-103">Criar policyset</span><span class="sxs-lookup"><span data-stu-id="83f66-103">Create policySet</span></span>

> <span data-ttu-id="83f66-104">**Importante:** As APIs do Microsoft Graph na versão/beta estão sujeitas a alterações; Não há suporte para o uso de produção.</span><span class="sxs-lookup"><span data-stu-id="83f66-104">**Important:** Microsoft Graph APIs under the /beta version are subject to change; production use is not supported.</span></span>

> <span data-ttu-id="83f66-105">**Observação:** A API do Microsoft Graph para Intune requer uma [licença do Active Intune](https://go.microsoft.com/fwlink/?linkid=839381) para o locatário.</span><span class="sxs-lookup"><span data-stu-id="83f66-105">**Note:** The Microsoft Graph API for Intune requires an [active Intune license](https://go.microsoft.com/fwlink/?linkid=839381) for the tenant.</span></span>

<span data-ttu-id="83f66-106">Criar um novo objeto [policyset](../resources/intune-policyset-policyset.md) .</span><span class="sxs-lookup"><span data-stu-id="83f66-106">Create a new [policySet](../resources/intune-policyset-policyset.md) object.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="83f66-107">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="83f66-107">Prerequisites</span></span>
<span data-ttu-id="83f66-p101">Uma das seguintes permissões é obrigatória para chamar esta API. Para saber mais, incluindo como escolher permissões, confira [Permissões](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="83f66-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="83f66-110">Tipo de permissão</span><span class="sxs-lookup"><span data-stu-id="83f66-110">Permission type</span></span>|<span data-ttu-id="83f66-111">Permissões (de privilégios máximos a mínimos)</span><span class="sxs-lookup"><span data-stu-id="83f66-111">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="83f66-112">Delegado (conta corporativa ou de estudante)</span><span class="sxs-lookup"><span data-stu-id="83f66-112">Delegated (work or school account)</span></span>|<span data-ttu-id="83f66-113">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="83f66-113">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="83f66-114">Delegado (conta pessoal da Microsoft)</span><span class="sxs-lookup"><span data-stu-id="83f66-114">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="83f66-115">Sem suporte.</span><span class="sxs-lookup"><span data-stu-id="83f66-115">Not supported.</span></span>|
|<span data-ttu-id="83f66-116">Aplicativo</span><span class="sxs-lookup"><span data-stu-id="83f66-116">Application</span></span>|<span data-ttu-id="83f66-117">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="83f66-117">DeviceManagementConfiguration.ReadWrite.All</span></span>|

## <a name="http-request"></a><span data-ttu-id="83f66-118">Solicitação HTTP</span><span class="sxs-lookup"><span data-stu-id="83f66-118">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/policySets
```

## <a name="request-headers"></a><span data-ttu-id="83f66-119">Cabeçalhos de solicitação</span><span class="sxs-lookup"><span data-stu-id="83f66-119">Request headers</span></span>
|<span data-ttu-id="83f66-120">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="83f66-120">Header</span></span>|<span data-ttu-id="83f66-121">Valor</span><span class="sxs-lookup"><span data-stu-id="83f66-121">Value</span></span>|
|:---|:---|
|<span data-ttu-id="83f66-122">Autorização</span><span class="sxs-lookup"><span data-stu-id="83f66-122">Authorization</span></span>|<span data-ttu-id="83f66-123">&lt;Token&gt; de portador obrigatório.</span><span class="sxs-lookup"><span data-stu-id="83f66-123">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="83f66-124">Aceitar</span><span class="sxs-lookup"><span data-stu-id="83f66-124">Accept</span></span>|<span data-ttu-id="83f66-125">application/json</span><span class="sxs-lookup"><span data-stu-id="83f66-125">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="83f66-126">Corpo da solicitação</span><span class="sxs-lookup"><span data-stu-id="83f66-126">Request body</span></span>
<span data-ttu-id="83f66-127">No corpo da solicitação, forneça uma representação JSON do objeto policyset.</span><span class="sxs-lookup"><span data-stu-id="83f66-127">In the request body, supply a JSON representation for the policySet object.</span></span>

<span data-ttu-id="83f66-128">A tabela a seguir mostra as propriedades que são necessárias ao criar o policyset.</span><span class="sxs-lookup"><span data-stu-id="83f66-128">The following table shows the properties that are required when you create the policySet.</span></span>

|<span data-ttu-id="83f66-129">Propriedade</span><span class="sxs-lookup"><span data-stu-id="83f66-129">Property</span></span>|<span data-ttu-id="83f66-130">Tipo</span><span class="sxs-lookup"><span data-stu-id="83f66-130">Type</span></span>|<span data-ttu-id="83f66-131">Descrição</span><span class="sxs-lookup"><span data-stu-id="83f66-131">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="83f66-132">id</span><span class="sxs-lookup"><span data-stu-id="83f66-132">id</span></span>|<span data-ttu-id="83f66-133">Cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="83f66-133">String</span></span>|<span data-ttu-id="83f66-134">Chave do Policyset.</span><span class="sxs-lookup"><span data-stu-id="83f66-134">Key of the PolicySet.</span></span>|
|<span data-ttu-id="83f66-135">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="83f66-135">createdDateTime</span></span>|<span data-ttu-id="83f66-136">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="83f66-136">DateTimeOffset</span></span>|<span data-ttu-id="83f66-137">Hora de criação do Policyset.</span><span class="sxs-lookup"><span data-stu-id="83f66-137">Creation time of the PolicySet.</span></span>|
|<span data-ttu-id="83f66-138">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="83f66-138">lastModifiedDateTime</span></span>|<span data-ttu-id="83f66-139">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="83f66-139">DateTimeOffset</span></span>|<span data-ttu-id="83f66-140">Hora da última modificação do Policyset.</span><span class="sxs-lookup"><span data-stu-id="83f66-140">Last modified time of the PolicySet.</span></span>|
|<span data-ttu-id="83f66-141">displayName</span><span class="sxs-lookup"><span data-stu-id="83f66-141">displayName</span></span>|<span data-ttu-id="83f66-142">String</span><span class="sxs-lookup"><span data-stu-id="83f66-142">String</span></span>|<span data-ttu-id="83f66-143">DisplayName do Policyset.</span><span class="sxs-lookup"><span data-stu-id="83f66-143">DisplayName of the PolicySet.</span></span>|
|<span data-ttu-id="83f66-144">descrição</span><span class="sxs-lookup"><span data-stu-id="83f66-144">description</span></span>|<span data-ttu-id="83f66-145">String</span><span class="sxs-lookup"><span data-stu-id="83f66-145">String</span></span>|<span data-ttu-id="83f66-146">Descrição do Policyset.</span><span class="sxs-lookup"><span data-stu-id="83f66-146">Description of the PolicySet.</span></span>|
|<span data-ttu-id="83f66-147">status</span><span class="sxs-lookup"><span data-stu-id="83f66-147">status</span></span>|[<span data-ttu-id="83f66-148">policySetStatus</span><span class="sxs-lookup"><span data-stu-id="83f66-148">policySetStatus</span></span>](../resources/intune-policyset-policysetstatus.md)|<span data-ttu-id="83f66-149">Status de validação/atribuição do Policyset.</span><span class="sxs-lookup"><span data-stu-id="83f66-149">Validation/assignment status of the PolicySet.</span></span> <span data-ttu-id="83f66-150">Os valores possíveis são: `unknown`, `validating`, `partialSuccess`, `success`, `error`, `notAssigned`.</span><span class="sxs-lookup"><span data-stu-id="83f66-150">Possible values are: `unknown`, `validating`, `partialSuccess`, `success`, `error`, `notAssigned`.</span></span>|
|<span data-ttu-id="83f66-151">errorCode</span><span class="sxs-lookup"><span data-stu-id="83f66-151">errorCode</span></span>|[<span data-ttu-id="83f66-152">errorCode</span><span class="sxs-lookup"><span data-stu-id="83f66-152">errorCode</span></span>](../resources/intune-policyset-errorcode.md)|<span data-ttu-id="83f66-153">Código de erro, caso algum tenha ocorrido.</span><span class="sxs-lookup"><span data-stu-id="83f66-153">Error code if any occured.</span></span> <span data-ttu-id="83f66-154">Os valores possíveis são: `noError`, `unauthorized`, `notFound`, `deleted`.</span><span class="sxs-lookup"><span data-stu-id="83f66-154">Possible values are: `noError`, `unauthorized`, `notFound`, `deleted`.</span></span>|
|<span data-ttu-id="83f66-155">guidedDeploymentTags</span><span class="sxs-lookup"><span data-stu-id="83f66-155">guidedDeploymentTags</span></span>|<span data-ttu-id="83f66-156">Coleção de cadeias de caracteres</span><span class="sxs-lookup"><span data-stu-id="83f66-156">String collection</span></span>|<span data-ttu-id="83f66-157">Marcas da implantação dirigida</span><span class="sxs-lookup"><span data-stu-id="83f66-157">Tags of the guided deployment</span></span>|
|<span data-ttu-id="83f66-158">roleScopeTags</span><span class="sxs-lookup"><span data-stu-id="83f66-158">roleScopeTags</span></span>|<span data-ttu-id="83f66-159">Coleção de cadeias de caracteres</span><span class="sxs-lookup"><span data-stu-id="83f66-159">String collection</span></span>|<span data-ttu-id="83f66-160">RoleScopeTags do Policyset</span><span class="sxs-lookup"><span data-stu-id="83f66-160">RoleScopeTags of the PolicySet</span></span>|



## <a name="response"></a><span data-ttu-id="83f66-161">Resposta</span><span class="sxs-lookup"><span data-stu-id="83f66-161">Response</span></span>
<span data-ttu-id="83f66-162">Se tiver êxito, este método retornará `201 Created` um código de resposta e um objeto [policyset](../resources/intune-policyset-policyset.md) no corpo da resposta.</span><span class="sxs-lookup"><span data-stu-id="83f66-162">If successful, this method returns a `201 Created` response code and a [policySet](../resources/intune-policyset-policyset.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="83f66-163">Exemplo</span><span class="sxs-lookup"><span data-stu-id="83f66-163">Example</span></span>

### <a name="request"></a><span data-ttu-id="83f66-164">Solicitação</span><span class="sxs-lookup"><span data-stu-id="83f66-164">Request</span></span>
<span data-ttu-id="83f66-165">Este é um exemplo da solicitação.</span><span class="sxs-lookup"><span data-stu-id="83f66-165">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceAppManagement/policySets
Content-type: application/json
Content-length: 317

{
  "@odata.type": "#microsoft.graph.policySet",
  "displayName": "Display Name value",
  "description": "Description value",
  "status": "validating",
  "errorCode": "unauthorized",
  "guidedDeploymentTags": [
    "Guided Deployment Tags value"
  ],
  "roleScopeTags": [
    "Role Scope Tags value"
  ]
}
```

### <a name="response"></a><span data-ttu-id="83f66-166">Resposta</span><span class="sxs-lookup"><span data-stu-id="83f66-166">Response</span></span>
<span data-ttu-id="83f66-p104">Veja a seguir um exemplo da resposta. Observação: o objeto response mostrado aqui pode estar truncado por motivos de concisão. Todas as propriedades serão retornadas de uma chamada real.</span><span class="sxs-lookup"><span data-stu-id="83f66-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 489

{
  "@odata.type": "#microsoft.graph.policySet",
  "id": "653cb373-b373-653c-73b3-3c6573b33c65",
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "displayName": "Display Name value",
  "description": "Description value",
  "status": "validating",
  "errorCode": "unauthorized",
  "guidedDeploymentTags": [
    "Guided Deployment Tags value"
  ],
  "roleScopeTags": [
    "Role Scope Tags value"
  ]
}
```



