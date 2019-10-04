---
title: atribuir ação
description: Ainda não documentado
author: rolyon
localization_priority: Normal
ms.prod: Intune
doc_type: apiPageType
ms.openlocfilehash: ea8fe89a9cf63471027aa8c6840835f632d43d78
ms.sourcegitcommit: 86903a4730bbd825eabb7f0a1b2429723cc8b1e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/26/2019
ms.locfileid: "37199443"
---
# <a name="assign-action"></a><span data-ttu-id="18d4b-103">atribuir ação</span><span class="sxs-lookup"><span data-stu-id="18d4b-103">assign action</span></span>

> <span data-ttu-id="18d4b-104">**Importante:** As APIs do Microsoft Graph na versão/beta estão sujeitas a alterações; Não há suporte para o uso de produção.</span><span class="sxs-lookup"><span data-stu-id="18d4b-104">**Important:** Microsoft Graph APIs under the /beta version are subject to change; production use is not supported.</span></span>

> <span data-ttu-id="18d4b-105">**Observação:** A API do Microsoft Graph para Intune requer uma [licença do Active Intune](https://go.microsoft.com/fwlink/?linkid=839381) para o locatário.</span><span class="sxs-lookup"><span data-stu-id="18d4b-105">**Note:** The Microsoft Graph API for Intune requires an [active Intune license](https://go.microsoft.com/fwlink/?linkid=839381) for the tenant.</span></span>

<span data-ttu-id="18d4b-106">Ainda não documentado</span><span class="sxs-lookup"><span data-stu-id="18d4b-106">Not yet documented</span></span>

## <a name="prerequisites"></a><span data-ttu-id="18d4b-107">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="18d4b-107">Prerequisites</span></span>
<span data-ttu-id="18d4b-p101">Uma das seguintes permissões é obrigatória para chamar esta API. Para saber mais, incluindo como escolher permissões, confira [Permissões](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="18d4b-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="18d4b-110">Tipo de permissão</span><span class="sxs-lookup"><span data-stu-id="18d4b-110">Permission type</span></span>|<span data-ttu-id="18d4b-111">Permissões (de privilégios máximos a mínimos)</span><span class="sxs-lookup"><span data-stu-id="18d4b-111">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="18d4b-112">Delegado (conta corporativa ou de estudante)</span><span class="sxs-lookup"><span data-stu-id="18d4b-112">Delegated (work or school account)</span></span>||
| <span data-ttu-id="18d4b-113">&nbsp; &nbsp; **Integração**</span><span class="sxs-lookup"><span data-stu-id="18d4b-113">&nbsp; &nbsp; **Onboarding**</span></span> | <span data-ttu-id="18d4b-114">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="18d4b-114">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="18d4b-115">Delegado (conta pessoal da Microsoft)</span><span class="sxs-lookup"><span data-stu-id="18d4b-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="18d4b-116">Sem suporte.</span><span class="sxs-lookup"><span data-stu-id="18d4b-116">Not supported.</span></span>|
|<span data-ttu-id="18d4b-117">Aplicativo</span><span class="sxs-lookup"><span data-stu-id="18d4b-117">Application</span></span>||
| <span data-ttu-id="18d4b-118">&nbsp; &nbsp; **Integração**</span><span class="sxs-lookup"><span data-stu-id="18d4b-118">&nbsp; &nbsp; **Onboarding**</span></span> | <span data-ttu-id="18d4b-119">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="18d4b-119">DeviceManagementServiceConfig.ReadWrite.All</span></span>|

## <a name="http-request"></a><span data-ttu-id="18d4b-120">Solicitação HTTP</span><span class="sxs-lookup"><span data-stu-id="18d4b-120">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceEnrollmentConfigurations/{deviceEnrollmentConfigurationId}/assign
```

## <a name="request-headers"></a><span data-ttu-id="18d4b-121">Cabeçalhos de solicitação</span><span class="sxs-lookup"><span data-stu-id="18d4b-121">Request headers</span></span>
|<span data-ttu-id="18d4b-122">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="18d4b-122">Header</span></span>|<span data-ttu-id="18d4b-123">Valor</span><span class="sxs-lookup"><span data-stu-id="18d4b-123">Value</span></span>|
|:---|:---|
|<span data-ttu-id="18d4b-124">Autorização</span><span class="sxs-lookup"><span data-stu-id="18d4b-124">Authorization</span></span>|<span data-ttu-id="18d4b-125">&lt;Token&gt; de portador obrigatório.</span><span class="sxs-lookup"><span data-stu-id="18d4b-125">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="18d4b-126">Aceitar</span><span class="sxs-lookup"><span data-stu-id="18d4b-126">Accept</span></span>|<span data-ttu-id="18d4b-127">application/json</span><span class="sxs-lookup"><span data-stu-id="18d4b-127">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="18d4b-128">Corpo da solicitação</span><span class="sxs-lookup"><span data-stu-id="18d4b-128">Request body</span></span>
<span data-ttu-id="18d4b-129">No corpo da solicitação, forneça uma representação JSON dos parâmetros.</span><span class="sxs-lookup"><span data-stu-id="18d4b-129">In the request body, supply JSON representation of the parameters.</span></span>

<span data-ttu-id="18d4b-130">A tabela a seguir mostra os parâmetros que podem ser usados com esta ação.</span><span class="sxs-lookup"><span data-stu-id="18d4b-130">The following table shows the parameters that can be used with this action.</span></span>

|<span data-ttu-id="18d4b-131">Propriedade</span><span class="sxs-lookup"><span data-stu-id="18d4b-131">Property</span></span>|<span data-ttu-id="18d4b-132">Tipo</span><span class="sxs-lookup"><span data-stu-id="18d4b-132">Type</span></span>|<span data-ttu-id="18d4b-133">Descrição</span><span class="sxs-lookup"><span data-stu-id="18d4b-133">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="18d4b-134">enrollmentConfigurationAssignments</span><span class="sxs-lookup"><span data-stu-id="18d4b-134">enrollmentConfigurationAssignments</span></span>|<span data-ttu-id="18d4b-135">Conjunto [enrollmentConfigurationAssignment](../resources/intune-onboarding-enrollmentconfigurationassignment.md)</span><span class="sxs-lookup"><span data-stu-id="18d4b-135">[enrollmentConfigurationAssignment](../resources/intune-onboarding-enrollmentconfigurationassignment.md) collection</span></span>|<span data-ttu-id="18d4b-136">Ainda não documentado</span><span class="sxs-lookup"><span data-stu-id="18d4b-136">Not yet documented</span></span>|



## <a name="response"></a><span data-ttu-id="18d4b-137">Resposta</span><span class="sxs-lookup"><span data-stu-id="18d4b-137">Response</span></span>
<span data-ttu-id="18d4b-138">Se tiver êxito, esta ação retornará um código de resposta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="18d4b-138">If successful, this action returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="18d4b-139">Exemplo</span><span class="sxs-lookup"><span data-stu-id="18d4b-139">Example</span></span>

### <a name="request"></a><span data-ttu-id="18d4b-140">Solicitação</span><span class="sxs-lookup"><span data-stu-id="18d4b-140">Request</span></span>
<span data-ttu-id="18d4b-141">Este é um exemplo da solicitação.</span><span class="sxs-lookup"><span data-stu-id="18d4b-141">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/deviceEnrollmentConfigurations/{deviceEnrollmentConfigurationId}/assign

Content-type: application/json
Content-length: 304

{
  "enrollmentConfigurationAssignments": [
    {
      "@odata.type": "#microsoft.graph.enrollmentConfigurationAssignment",
      "id": "705b021c-021c-705b-1c02-5b701c025b70",
      "target": {
        "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
      }
    }
  ]
}
```

### <a name="response"></a><span data-ttu-id="18d4b-142">Resposta</span><span class="sxs-lookup"><span data-stu-id="18d4b-142">Response</span></span>
<span data-ttu-id="18d4b-p102">Veja a seguir um exemplo da resposta. Observação: o objeto response mostrado aqui pode estar truncado por motivos de concisão. Todas as propriedades serão retornadas de uma chamada real.</span><span class="sxs-lookup"><span data-stu-id="18d4b-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 204 No Content
```



