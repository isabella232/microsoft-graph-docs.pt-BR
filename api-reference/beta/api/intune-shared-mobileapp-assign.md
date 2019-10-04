---
title: atribuir ação
description: Ainda não documentado
author: rolyon
localization_priority: Normal
ms.prod: Intune
doc_type: apiPageType
ms.openlocfilehash: a8917c1ec61104584136f329e64c578fd9f55a87
ms.sourcegitcommit: 86903a4730bbd825eabb7f0a1b2429723cc8b1e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/26/2019
ms.locfileid: "37199546"
---
# <a name="assign-action"></a><span data-ttu-id="a24ad-103">atribuir ação</span><span class="sxs-lookup"><span data-stu-id="a24ad-103">assign action</span></span>

> <span data-ttu-id="a24ad-104">**Importante:** As APIs do Microsoft Graph na versão/beta estão sujeitas a alterações; Não há suporte para o uso de produção.</span><span class="sxs-lookup"><span data-stu-id="a24ad-104">**Important:** Microsoft Graph APIs under the /beta version are subject to change; production use is not supported.</span></span>

> <span data-ttu-id="a24ad-105">**Observação:** A API do Microsoft Graph para Intune requer uma [licença do Active Intune](https://go.microsoft.com/fwlink/?linkid=839381) para o locatário.</span><span class="sxs-lookup"><span data-stu-id="a24ad-105">**Note:** The Microsoft Graph API for Intune requires an [active Intune license](https://go.microsoft.com/fwlink/?linkid=839381) for the tenant.</span></span>

<span data-ttu-id="a24ad-106">Ainda não documentado</span><span class="sxs-lookup"><span data-stu-id="a24ad-106">Not yet documented</span></span>

## <a name="prerequisites"></a><span data-ttu-id="a24ad-107">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="a24ad-107">Prerequisites</span></span>
<span data-ttu-id="a24ad-p101">Uma das seguintes permissões é obrigatória para chamar esta API. Para saber mais, incluindo como escolher permissões, confira [Permissões](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a24ad-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="a24ad-110">Tipo de permissão</span><span class="sxs-lookup"><span data-stu-id="a24ad-110">Permission type</span></span>|<span data-ttu-id="a24ad-111">Permissões (de privilégios máximos a mínimos)</span><span class="sxs-lookup"><span data-stu-id="a24ad-111">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="a24ad-112">Delegado (conta corporativa ou de estudante)</span><span class="sxs-lookup"><span data-stu-id="a24ad-112">Delegated (work or school account)</span></span>||
| <span data-ttu-id="a24ad-113">&nbsp;&nbsp; **Aplicativos**</span><span class="sxs-lookup"><span data-stu-id="a24ad-113">&nbsp; &nbsp; **Apps**</span></span> | <span data-ttu-id="a24ad-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="a24ad-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="a24ad-115">Delegado (conta pessoal da Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a24ad-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="a24ad-116">Sem suporte.</span><span class="sxs-lookup"><span data-stu-id="a24ad-116">Not supported.</span></span>|
|<span data-ttu-id="a24ad-117">Aplicativo</span><span class="sxs-lookup"><span data-stu-id="a24ad-117">Application</span></span>||
| <span data-ttu-id="a24ad-118">&nbsp;&nbsp; **Aplicativos**</span><span class="sxs-lookup"><span data-stu-id="a24ad-118">&nbsp; &nbsp; **Apps**</span></span> | <span data-ttu-id="a24ad-119">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="a24ad-119">DeviceManagementApps.ReadWrite.All</span></span>|

## <a name="http-request"></a><span data-ttu-id="a24ad-120">Solicitação HTTP</span><span class="sxs-lookup"><span data-stu-id="a24ad-120">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/mobileApps/{mobileAppId}/assign
POST /deviceAppManagement/mobileApps/{mobileAppId}/userStatuses/{userAppInstallStatusId}/app/assign
POST /deviceAppManagement/mobileApps/{mobileAppId}/deviceStatuses/{mobileAppInstallStatusId}/app/assign
```

## <a name="request-headers"></a><span data-ttu-id="a24ad-121">Cabeçalhos de solicitação</span><span class="sxs-lookup"><span data-stu-id="a24ad-121">Request headers</span></span>
|<span data-ttu-id="a24ad-122">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="a24ad-122">Header</span></span>|<span data-ttu-id="a24ad-123">Valor</span><span class="sxs-lookup"><span data-stu-id="a24ad-123">Value</span></span>|
|:---|:---|
|<span data-ttu-id="a24ad-124">Autorização</span><span class="sxs-lookup"><span data-stu-id="a24ad-124">Authorization</span></span>|<span data-ttu-id="a24ad-125">&lt;Token&gt; de portador obrigatório.</span><span class="sxs-lookup"><span data-stu-id="a24ad-125">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="a24ad-126">Aceitar</span><span class="sxs-lookup"><span data-stu-id="a24ad-126">Accept</span></span>|<span data-ttu-id="a24ad-127">application/json</span><span class="sxs-lookup"><span data-stu-id="a24ad-127">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="a24ad-128">Corpo da solicitação</span><span class="sxs-lookup"><span data-stu-id="a24ad-128">Request body</span></span>
<span data-ttu-id="a24ad-129">No corpo da solicitação, forneça uma representação JSON dos parâmetros.</span><span class="sxs-lookup"><span data-stu-id="a24ad-129">In the request body, supply JSON representation of the parameters.</span></span>

<span data-ttu-id="a24ad-130">A tabela a seguir mostra os parâmetros que podem ser usados com esta ação.</span><span class="sxs-lookup"><span data-stu-id="a24ad-130">The following table shows the parameters that can be used with this action.</span></span>

|<span data-ttu-id="a24ad-131">Propriedade</span><span class="sxs-lookup"><span data-stu-id="a24ad-131">Property</span></span>|<span data-ttu-id="a24ad-132">Tipo</span><span class="sxs-lookup"><span data-stu-id="a24ad-132">Type</span></span>|<span data-ttu-id="a24ad-133">Descrição</span><span class="sxs-lookup"><span data-stu-id="a24ad-133">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="a24ad-134">mobileAppAssignments</span><span class="sxs-lookup"><span data-stu-id="a24ad-134">mobileAppAssignments</span></span>|<span data-ttu-id="a24ad-135">Coleção [mobileAppAssignment](../resources/intune-apps-mobileappassignment.md)</span><span class="sxs-lookup"><span data-stu-id="a24ad-135">[mobileAppAssignment](../resources/intune-apps-mobileappassignment.md) collection</span></span>|<span data-ttu-id="a24ad-136">Ainda não documentado</span><span class="sxs-lookup"><span data-stu-id="a24ad-136">Not yet documented</span></span>|



## <a name="response"></a><span data-ttu-id="a24ad-137">Resposta</span><span class="sxs-lookup"><span data-stu-id="a24ad-137">Response</span></span>
<span data-ttu-id="a24ad-138">Se tiver êxito, esta ação retornará um código de resposta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="a24ad-138">If successful, this action returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="a24ad-139">Exemplo</span><span class="sxs-lookup"><span data-stu-id="a24ad-139">Example</span></span>

### <a name="request"></a><span data-ttu-id="a24ad-140">Solicitação</span><span class="sxs-lookup"><span data-stu-id="a24ad-140">Request</span></span>
<span data-ttu-id="a24ad-141">Este é um exemplo da solicitação.</span><span class="sxs-lookup"><span data-stu-id="a24ad-141">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceAppManagement/mobileApps/{mobileAppId}/assign

Content-type: application/json
Content-length: 406

{
  "mobileAppAssignments": [
    {
      "@odata.type": "#microsoft.graph.mobileAppAssignment",
      "id": "591620b7-20b7-5916-b720-1659b7201659",
      "intent": "required",
      "target": {
        "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
      },
      "settings": {
        "@odata.type": "microsoft.graph.mobileAppAssignmentSettings"
      }
    }
  ]
}
```

### <a name="response"></a><span data-ttu-id="a24ad-142">Resposta</span><span class="sxs-lookup"><span data-stu-id="a24ad-142">Response</span></span>
<span data-ttu-id="a24ad-p102">Veja a seguir um exemplo da resposta. Observação: o objeto response mostrado aqui pode estar truncado por motivos de concisão. Todas as propriedades serão retornadas de uma chamada real.</span><span class="sxs-lookup"><span data-stu-id="a24ad-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 204 No Content
```



