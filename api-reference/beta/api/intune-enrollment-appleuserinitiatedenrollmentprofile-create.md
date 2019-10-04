---
title: Criar appleUserInitiatedEnrollmentProfile
description: Criar um novo objeto appleUserInitiatedEnrollmentProfile.
author: rolyon
localization_priority: Normal
ms.prod: Intune
doc_type: apiPageType
ms.openlocfilehash: 447089b67e9151a9f2310b3368c01ef05f9a80e0
ms.sourcegitcommit: 86903a4730bbd825eabb7f0a1b2429723cc8b1e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/26/2019
ms.locfileid: "37191677"
---
# <a name="create-appleuserinitiatedenrollmentprofile"></a><span data-ttu-id="c1be6-103">Criar appleUserInitiatedEnrollmentProfile</span><span class="sxs-lookup"><span data-stu-id="c1be6-103">Create appleUserInitiatedEnrollmentProfile</span></span>

> <span data-ttu-id="c1be6-104">**Importante:** As APIs do Microsoft Graph na versão/beta estão sujeitas a alterações; Não há suporte para o uso de produção.</span><span class="sxs-lookup"><span data-stu-id="c1be6-104">**Important:** Microsoft Graph APIs under the /beta version are subject to change; production use is not supported.</span></span>

> <span data-ttu-id="c1be6-105">**Observação:** A API do Microsoft Graph para Intune requer uma [licença do Active Intune](https://go.microsoft.com/fwlink/?linkid=839381) para o locatário.</span><span class="sxs-lookup"><span data-stu-id="c1be6-105">**Note:** The Microsoft Graph API for Intune requires an [active Intune license](https://go.microsoft.com/fwlink/?linkid=839381) for the tenant.</span></span>

<span data-ttu-id="c1be6-106">Criar um novo objeto [appleUserInitiatedEnrollmentProfile](../resources/intune-enrollment-appleuserinitiatedenrollmentprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="c1be6-106">Create a new [appleUserInitiatedEnrollmentProfile](../resources/intune-enrollment-appleuserinitiatedenrollmentprofile.md) object.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="c1be6-107">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="c1be6-107">Prerequisites</span></span>
<span data-ttu-id="c1be6-p101">Uma das seguintes permissões é obrigatória para chamar esta API. Para saber mais, incluindo como escolher permissões, confira [Permissões](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="c1be6-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="c1be6-110">Tipo de permissão</span><span class="sxs-lookup"><span data-stu-id="c1be6-110">Permission type</span></span>|<span data-ttu-id="c1be6-111">Permissões (de privilégios máximos a mínimos)</span><span class="sxs-lookup"><span data-stu-id="c1be6-111">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="c1be6-112">Delegado (conta corporativa ou de estudante)</span><span class="sxs-lookup"><span data-stu-id="c1be6-112">Delegated (work or school account)</span></span>|<span data-ttu-id="c1be6-113">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="c1be6-113">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="c1be6-114">Delegado (conta pessoal da Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c1be6-114">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="c1be6-115">Sem suporte.</span><span class="sxs-lookup"><span data-stu-id="c1be6-115">Not supported.</span></span>|
|<span data-ttu-id="c1be6-116">Aplicativo</span><span class="sxs-lookup"><span data-stu-id="c1be6-116">Application</span></span>|<span data-ttu-id="c1be6-117">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="c1be6-117">DeviceManagementServiceConfig.ReadWrite.All</span></span>|

## <a name="http-request"></a><span data-ttu-id="c1be6-118">Solicitação HTTP</span><span class="sxs-lookup"><span data-stu-id="c1be6-118">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/appleUserInitiatedEnrollmentProfiles
```

## <a name="request-headers"></a><span data-ttu-id="c1be6-119">Cabeçalhos de solicitação</span><span class="sxs-lookup"><span data-stu-id="c1be6-119">Request headers</span></span>
|<span data-ttu-id="c1be6-120">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="c1be6-120">Header</span></span>|<span data-ttu-id="c1be6-121">Valor</span><span class="sxs-lookup"><span data-stu-id="c1be6-121">Value</span></span>|
|:---|:---|
|<span data-ttu-id="c1be6-122">Autorização</span><span class="sxs-lookup"><span data-stu-id="c1be6-122">Authorization</span></span>|<span data-ttu-id="c1be6-123">&lt;Token&gt; de portador obrigatório.</span><span class="sxs-lookup"><span data-stu-id="c1be6-123">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="c1be6-124">Aceitar</span><span class="sxs-lookup"><span data-stu-id="c1be6-124">Accept</span></span>|<span data-ttu-id="c1be6-125">application/json</span><span class="sxs-lookup"><span data-stu-id="c1be6-125">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="c1be6-126">Corpo da solicitação</span><span class="sxs-lookup"><span data-stu-id="c1be6-126">Request body</span></span>
<span data-ttu-id="c1be6-127">No corpo da solicitação, forneça uma representação JSON do objeto appleUserInitiatedEnrollmentProfile.</span><span class="sxs-lookup"><span data-stu-id="c1be6-127">In the request body, supply a JSON representation for the appleUserInitiatedEnrollmentProfile object.</span></span>

<span data-ttu-id="c1be6-128">A tabela a seguir mostra as propriedades que são necessárias ao criar appleUserInitiatedEnrollmentProfile.</span><span class="sxs-lookup"><span data-stu-id="c1be6-128">The following table shows the properties that are required when you create the appleUserInitiatedEnrollmentProfile.</span></span>

|<span data-ttu-id="c1be6-129">Propriedade</span><span class="sxs-lookup"><span data-stu-id="c1be6-129">Property</span></span>|<span data-ttu-id="c1be6-130">Tipo</span><span class="sxs-lookup"><span data-stu-id="c1be6-130">Type</span></span>|<span data-ttu-id="c1be6-131">Descrição</span><span class="sxs-lookup"><span data-stu-id="c1be6-131">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="c1be6-132">defaultenrollmentidtype</span><span class="sxs-lookup"><span data-stu-id="c1be6-132">defaultEnrollmentType</span></span>|[<span data-ttu-id="c1be6-133">appleUserInitiatedEnrollmentType</span><span class="sxs-lookup"><span data-stu-id="c1be6-133">appleUserInitiatedEnrollmentType</span></span>](../resources/intune-enrollment-appleuserinitiatedenrollmenttype.md)|<span data-ttu-id="c1be6-134">O tipo de registro de perfil padrão.</span><span class="sxs-lookup"><span data-stu-id="c1be6-134">The default profile enrollment type.</span></span> <span data-ttu-id="c1be6-135">Os valores possíveis são: `unknown`, `device`, `user`.</span><span class="sxs-lookup"><span data-stu-id="c1be6-135">Possible values are: `unknown`, `device`, `user`.</span></span>|
|<span data-ttu-id="c1be6-136">availableEnrollmentTypeOptions</span><span class="sxs-lookup"><span data-stu-id="c1be6-136">availableEnrollmentTypeOptions</span></span>|<span data-ttu-id="c1be6-137">coleção [appleOwnerTypeEnrollmentType](../resources/intune-enrollment-appleownertypeenrollmenttype.md)</span><span class="sxs-lookup"><span data-stu-id="c1be6-137">[appleOwnerTypeEnrollmentType](../resources/intune-enrollment-appleownertypeenrollmenttype.md) collection</span></span>|<span data-ttu-id="c1be6-138">Lista de opções de tipo de registro disponíveis</span><span class="sxs-lookup"><span data-stu-id="c1be6-138">List of available enrollment type options</span></span>|
|<span data-ttu-id="c1be6-139">id</span><span class="sxs-lookup"><span data-stu-id="c1be6-139">id</span></span>|<span data-ttu-id="c1be6-140">Cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="c1be6-140">String</span></span>|<span data-ttu-id="c1be6-141">O GUID do objeto.</span><span class="sxs-lookup"><span data-stu-id="c1be6-141">The GUID for the object</span></span>|
|<span data-ttu-id="c1be6-142">displayName</span><span class="sxs-lookup"><span data-stu-id="c1be6-142">displayName</span></span>|<span data-ttu-id="c1be6-143">String</span><span class="sxs-lookup"><span data-stu-id="c1be6-143">String</span></span>|<span data-ttu-id="c1be6-144">Nome do perfil</span><span class="sxs-lookup"><span data-stu-id="c1be6-144">Name of the profile</span></span>|
|<span data-ttu-id="c1be6-145">descrição</span><span class="sxs-lookup"><span data-stu-id="c1be6-145">description</span></span>|<span data-ttu-id="c1be6-146">String</span><span class="sxs-lookup"><span data-stu-id="c1be6-146">String</span></span>|<span data-ttu-id="c1be6-147">Descrição do perfil</span><span class="sxs-lookup"><span data-stu-id="c1be6-147">Description of the profile</span></span>|
|<span data-ttu-id="c1be6-148">prioridade</span><span class="sxs-lookup"><span data-stu-id="c1be6-148">priority</span></span>|<span data-ttu-id="c1be6-149">Int32</span><span class="sxs-lookup"><span data-stu-id="c1be6-149">Int32</span></span>|<span data-ttu-id="c1be6-150">Prioridade, 0 é a maior</span><span class="sxs-lookup"><span data-stu-id="c1be6-150">Priority, 0 is highest</span></span>|
|<span data-ttu-id="c1be6-151">platform</span><span class="sxs-lookup"><span data-stu-id="c1be6-151">platform</span></span>|[<span data-ttu-id="c1be6-152">devicePlatformType</span><span class="sxs-lookup"><span data-stu-id="c1be6-152">devicePlatformType</span></span>](../resources/intune-shared-deviceplatformtype.md)|<span data-ttu-id="c1be6-153">A plataforma do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c1be6-153">The platform of the Device.</span></span> <span data-ttu-id="c1be6-154">Os valores possíveis são: `android`, `androidForWork`, `iOS`, `macOS`, `windowsPhone81`, `windows81AndLater`, `windows10AndLater`, `androidWorkProfile`, `unknown`.</span><span class="sxs-lookup"><span data-stu-id="c1be6-154">Possible values are: `android`, `androidForWork`, `iOS`, `macOS`, `windowsPhone81`, `windows81AndLater`, `windows10AndLater`, `androidWorkProfile`, `unknown`.</span></span>|
|<span data-ttu-id="c1be6-155">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="c1be6-155">createdDateTime</span></span>|<span data-ttu-id="c1be6-156">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="c1be6-156">DateTimeOffset</span></span>|<span data-ttu-id="c1be6-157">Hora de criação do perfil</span><span class="sxs-lookup"><span data-stu-id="c1be6-157">Profile creation time</span></span>|
|<span data-ttu-id="c1be6-158">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="c1be6-158">lastModifiedDateTime</span></span>|<span data-ttu-id="c1be6-159">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="c1be6-159">DateTimeOffset</span></span>|<span data-ttu-id="c1be6-160">Hora da última modificação do perfil</span><span class="sxs-lookup"><span data-stu-id="c1be6-160">Profile last modified time</span></span>|



## <a name="response"></a><span data-ttu-id="c1be6-161">Resposta</span><span class="sxs-lookup"><span data-stu-id="c1be6-161">Response</span></span>
<span data-ttu-id="c1be6-162">Se tiver êxito, este método retornará `201 Created` um código de resposta e um objeto [appleUserInitiatedEnrollmentProfile](../resources/intune-enrollment-appleuserinitiatedenrollmentprofile.md) no corpo da resposta.</span><span class="sxs-lookup"><span data-stu-id="c1be6-162">If successful, this method returns a `201 Created` response code and a [appleUserInitiatedEnrollmentProfile](../resources/intune-enrollment-appleuserinitiatedenrollmentprofile.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="c1be6-163">Exemplo</span><span class="sxs-lookup"><span data-stu-id="c1be6-163">Example</span></span>

### <a name="request"></a><span data-ttu-id="c1be6-164">Solicitação</span><span class="sxs-lookup"><span data-stu-id="c1be6-164">Request</span></span>
<span data-ttu-id="c1be6-165">Este é um exemplo da solicitação.</span><span class="sxs-lookup"><span data-stu-id="c1be6-165">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/appleUserInitiatedEnrollmentProfiles
Content-type: application/json
Content-length: 439

{
  "@odata.type": "#microsoft.graph.appleUserInitiatedEnrollmentProfile",
  "defaultEnrollmentType": "device",
  "availableEnrollmentTypeOptions": [
    {
      "@odata.type": "microsoft.graph.appleOwnerTypeEnrollmentType",
      "ownerType": "company",
      "enrollmentType": "device"
    }
  ],
  "displayName": "Display Name value",
  "description": "Description value",
  "priority": 8,
  "platform": "androidForWork"
}
```

### <a name="response"></a><span data-ttu-id="c1be6-166">Resposta</span><span class="sxs-lookup"><span data-stu-id="c1be6-166">Response</span></span>
<span data-ttu-id="c1be6-p104">Veja a seguir um exemplo da resposta. Observação: o objeto response mostrado aqui pode estar truncado por motivos de concisão. Todas as propriedades serão retornadas de uma chamada real.</span><span class="sxs-lookup"><span data-stu-id="c1be6-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 611

{
  "@odata.type": "#microsoft.graph.appleUserInitiatedEnrollmentProfile",
  "defaultEnrollmentType": "device",
  "availableEnrollmentTypeOptions": [
    {
      "@odata.type": "microsoft.graph.appleOwnerTypeEnrollmentType",
      "ownerType": "company",
      "enrollmentType": "device"
    }
  ],
  "id": "5a11d98e-d98e-5a11-8ed9-115a8ed9115a",
  "displayName": "Display Name value",
  "description": "Description value",
  "priority": 8,
  "platform": "androidForWork",
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00"
}
```



