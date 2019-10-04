---
title: ação hasPayloadLinks
description: Ainda não documentado
author: rolyon
localization_priority: Normal
ms.prod: Intune
doc_type: apiPageType
ms.openlocfilehash: 8042ba202715d947e69191ae6c94950afc6c39f9
ms.sourcegitcommit: 86903a4730bbd825eabb7f0a1b2429723cc8b1e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/26/2019
ms.locfileid: "37191791"
---
# <a name="haspayloadlinks-action"></a><span data-ttu-id="2a6b0-103">ação hasPayloadLinks</span><span class="sxs-lookup"><span data-stu-id="2a6b0-103">hasPayloadLinks action</span></span>

> <span data-ttu-id="2a6b0-104">**Importante:** As APIs do Microsoft Graph na versão/beta estão sujeitas a alterações; Não há suporte para o uso de produção.</span><span class="sxs-lookup"><span data-stu-id="2a6b0-104">**Important:** Microsoft Graph APIs under the /beta version are subject to change; production use is not supported.</span></span>

> <span data-ttu-id="2a6b0-105">**Observação:** A API do Microsoft Graph para Intune requer uma [licença do Active Intune](https://go.microsoft.com/fwlink/?linkid=839381) para o locatário.</span><span class="sxs-lookup"><span data-stu-id="2a6b0-105">**Note:** The Microsoft Graph API for Intune requires an [active Intune license](https://go.microsoft.com/fwlink/?linkid=839381) for the tenant.</span></span>

<span data-ttu-id="2a6b0-106">Ainda não documentado</span><span class="sxs-lookup"><span data-stu-id="2a6b0-106">Not yet documented</span></span>

## <a name="prerequisites"></a><span data-ttu-id="2a6b0-107">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="2a6b0-107">Prerequisites</span></span>
<span data-ttu-id="2a6b0-p101">Uma das seguintes permissões é obrigatória para chamar esta API. Para saber mais, incluindo como escolher permissões, confira [Permissões](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="2a6b0-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="2a6b0-110">Tipo de permissão</span><span class="sxs-lookup"><span data-stu-id="2a6b0-110">Permission type</span></span>|<span data-ttu-id="2a6b0-111">Permissões (de privilégios máximos a mínimos)</span><span class="sxs-lookup"><span data-stu-id="2a6b0-111">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="2a6b0-112">Delegado (conta corporativa ou de estudante)</span><span class="sxs-lookup"><span data-stu-id="2a6b0-112">Delegated (work or school account)</span></span>|<span data-ttu-id="2a6b0-113">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="2a6b0-113">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="2a6b0-114">Delegado (conta pessoal da Microsoft)</span><span class="sxs-lookup"><span data-stu-id="2a6b0-114">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="2a6b0-115">Sem suporte.</span><span class="sxs-lookup"><span data-stu-id="2a6b0-115">Not supported.</span></span>|
|<span data-ttu-id="2a6b0-116">Aplicativo</span><span class="sxs-lookup"><span data-stu-id="2a6b0-116">Application</span></span>|<span data-ttu-id="2a6b0-117">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="2a6b0-117">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|

## <a name="http-request"></a><span data-ttu-id="2a6b0-118">Solicitação HTTP</span><span class="sxs-lookup"><span data-stu-id="2a6b0-118">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/macManagedAppProtections/hasPayloadLinks
```

## <a name="request-headers"></a><span data-ttu-id="2a6b0-119">Cabeçalhos de solicitação</span><span class="sxs-lookup"><span data-stu-id="2a6b0-119">Request headers</span></span>
|<span data-ttu-id="2a6b0-120">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="2a6b0-120">Header</span></span>|<span data-ttu-id="2a6b0-121">Valor</span><span class="sxs-lookup"><span data-stu-id="2a6b0-121">Value</span></span>|
|:---|:---|
|<span data-ttu-id="2a6b0-122">Autorização</span><span class="sxs-lookup"><span data-stu-id="2a6b0-122">Authorization</span></span>|<span data-ttu-id="2a6b0-123">&lt;Token&gt; de portador obrigatório.</span><span class="sxs-lookup"><span data-stu-id="2a6b0-123">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="2a6b0-124">Aceitar</span><span class="sxs-lookup"><span data-stu-id="2a6b0-124">Accept</span></span>|<span data-ttu-id="2a6b0-125">application/json</span><span class="sxs-lookup"><span data-stu-id="2a6b0-125">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="2a6b0-126">Corpo da solicitação</span><span class="sxs-lookup"><span data-stu-id="2a6b0-126">Request body</span></span>
<span data-ttu-id="2a6b0-127">No corpo da solicitação, forneça uma representação JSON dos parâmetros.</span><span class="sxs-lookup"><span data-stu-id="2a6b0-127">In the request body, supply JSON representation of the parameters.</span></span>

<span data-ttu-id="2a6b0-128">A tabela a seguir mostra os parâmetros que podem ser usados com esta ação.</span><span class="sxs-lookup"><span data-stu-id="2a6b0-128">The following table shows the parameters that can be used with this action.</span></span>

|<span data-ttu-id="2a6b0-129">Propriedade</span><span class="sxs-lookup"><span data-stu-id="2a6b0-129">Property</span></span>|<span data-ttu-id="2a6b0-130">Tipo</span><span class="sxs-lookup"><span data-stu-id="2a6b0-130">Type</span></span>|<span data-ttu-id="2a6b0-131">Descrição</span><span class="sxs-lookup"><span data-stu-id="2a6b0-131">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="2a6b0-132">payloadIds</span><span class="sxs-lookup"><span data-stu-id="2a6b0-132">payloadIds</span></span>|<span data-ttu-id="2a6b0-133">String collection</span><span class="sxs-lookup"><span data-stu-id="2a6b0-133">String collection</span></span>|<span data-ttu-id="2a6b0-134">Ainda não documentado</span><span class="sxs-lookup"><span data-stu-id="2a6b0-134">Not yet documented</span></span>|



## <a name="response"></a><span data-ttu-id="2a6b0-135">Resposta</span><span class="sxs-lookup"><span data-stu-id="2a6b0-135">Response</span></span>
<span data-ttu-id="2a6b0-136">Se tiver êxito, esta ação retornará `200 OK` um código de resposta e uma coleção [hasPayloadLinkResultItem](../resources/intune-policyset-haspayloadlinkresultitem.md) no corpo da resposta.</span><span class="sxs-lookup"><span data-stu-id="2a6b0-136">If successful, this action returns a `200 OK` response code and a [hasPayloadLinkResultItem](../resources/intune-policyset-haspayloadlinkresultitem.md) collection in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="2a6b0-137">Exemplo</span><span class="sxs-lookup"><span data-stu-id="2a6b0-137">Example</span></span>

### <a name="request"></a><span data-ttu-id="2a6b0-138">Solicitação</span><span class="sxs-lookup"><span data-stu-id="2a6b0-138">Request</span></span>
<span data-ttu-id="2a6b0-139">Este é um exemplo da solicitação.</span><span class="sxs-lookup"><span data-stu-id="2a6b0-139">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceAppManagement/macManagedAppProtections/hasPayloadLinks

Content-type: application/json
Content-length: 53

{
  "payloadIds": [
    "Payload Ids value"
  ]
}
```

### <a name="response"></a><span data-ttu-id="2a6b0-140">Resposta</span><span class="sxs-lookup"><span data-stu-id="2a6b0-140">Response</span></span>
<span data-ttu-id="2a6b0-p102">Veja a seguir um exemplo da resposta. Observação: o objeto response mostrado aqui pode estar truncado por motivos de concisão. Todas as propriedades serão retornadas de uma chamada real.</span><span class="sxs-lookup"><span data-stu-id="2a6b0-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 249

{
  "value": [
    {
      "@odata.type": "microsoft.graph.hasPayloadLinkResultItem",
      "payloadId": "Payload Id value",
      "hasLink": true,
      "error": "Error value",
      "sources": [
        "policySets"
      ]
    }
  ]
}
```



