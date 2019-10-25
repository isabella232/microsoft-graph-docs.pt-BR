---
title: Listar macOSMicrosoftEdgeApps
description: Listar Propriedades e relações dos objetos macOSMicrosoftEdgeApp.
author: rolyon
localization_priority: Normal
ms.prod: Intune
doc_type: apiPageType
ms.openlocfilehash: 10dbb46345415f9f841ec8f74f7ebbb39a447aab
ms.sourcegitcommit: 0dcabe677927c259c2ddcefd0d5e2a2aef065e8b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/16/2019
ms.locfileid: "37535321"
---
# <a name="list-macosmicrosoftedgeapps"></a><span data-ttu-id="62325-103">Listar macOSMicrosoftEdgeApps</span><span class="sxs-lookup"><span data-stu-id="62325-103">List macOSMicrosoftEdgeApps</span></span>

> <span data-ttu-id="62325-104">**Importante:** As APIs do Microsoft Graph na versão/beta estão sujeitas a alterações; Não há suporte para o uso de produção.</span><span class="sxs-lookup"><span data-stu-id="62325-104">**Important:** Microsoft Graph APIs under the /beta version are subject to change; production use is not supported.</span></span>

> <span data-ttu-id="62325-105">**Observação:** A API do Microsoft Graph para Intune requer uma [licença do Active Intune](https://go.microsoft.com/fwlink/?linkid=839381) para o locatário.</span><span class="sxs-lookup"><span data-stu-id="62325-105">**Note:** The Microsoft Graph API for Intune requires an [active Intune license](https://go.microsoft.com/fwlink/?linkid=839381) for the tenant.</span></span>

<span data-ttu-id="62325-106">Listar Propriedades e relações dos objetos [macOSMicrosoftEdgeApp](../resources/intune-apps-macosmicrosoftedgeapp.md) .</span><span class="sxs-lookup"><span data-stu-id="62325-106">List properties and relationships of the [macOSMicrosoftEdgeApp](../resources/intune-apps-macosmicrosoftedgeapp.md) objects.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="62325-107">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="62325-107">Prerequisites</span></span>
<span data-ttu-id="62325-p101">Uma das seguintes permissões é obrigatória para chamar esta API. Para saber mais, incluindo como escolher permissões, confira [Permissões](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="62325-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="62325-110">Tipo de permissão</span><span class="sxs-lookup"><span data-stu-id="62325-110">Permission type</span></span>|<span data-ttu-id="62325-111">Permissões (de privilégios máximos a mínimos)</span><span class="sxs-lookup"><span data-stu-id="62325-111">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="62325-112">Delegado (conta corporativa ou de estudante)</span><span class="sxs-lookup"><span data-stu-id="62325-112">Delegated (work or school account)</span></span>|<span data-ttu-id="62325-113">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="62325-113">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="62325-114">Delegado (conta pessoal da Microsoft)</span><span class="sxs-lookup"><span data-stu-id="62325-114">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="62325-115">Sem suporte.</span><span class="sxs-lookup"><span data-stu-id="62325-115">Not supported.</span></span>|
|<span data-ttu-id="62325-116">Application</span><span class="sxs-lookup"><span data-stu-id="62325-116">Application</span></span>|<span data-ttu-id="62325-117">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="62325-117">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|

## <a name="http-request"></a><span data-ttu-id="62325-118">Solicitação HTTP</span><span class="sxs-lookup"><span data-stu-id="62325-118">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/mobileApps
```

## <a name="request-headers"></a><span data-ttu-id="62325-119">Cabeçalhos de solicitação</span><span class="sxs-lookup"><span data-stu-id="62325-119">Request headers</span></span>
|<span data-ttu-id="62325-120">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="62325-120">Header</span></span>|<span data-ttu-id="62325-121">Valor</span><span class="sxs-lookup"><span data-stu-id="62325-121">Value</span></span>|
|:---|:---|
|<span data-ttu-id="62325-122">Autorização</span><span class="sxs-lookup"><span data-stu-id="62325-122">Authorization</span></span>|<span data-ttu-id="62325-123">&lt;Token&gt; de portador obrigatório.</span><span class="sxs-lookup"><span data-stu-id="62325-123">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="62325-124">Aceitar</span><span class="sxs-lookup"><span data-stu-id="62325-124">Accept</span></span>|<span data-ttu-id="62325-125">application/json</span><span class="sxs-lookup"><span data-stu-id="62325-125">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="62325-126">Corpo da solicitação</span><span class="sxs-lookup"><span data-stu-id="62325-126">Request body</span></span>
<span data-ttu-id="62325-127">Não forneça um corpo de solicitação para esse método.</span><span class="sxs-lookup"><span data-stu-id="62325-127">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="62325-128">Resposta</span><span class="sxs-lookup"><span data-stu-id="62325-128">Response</span></span>
<span data-ttu-id="62325-129">Se tiver êxito, este método retornará `200 OK` um código de resposta e uma coleção de objetos [macOSMicrosoftEdgeApp](../resources/intune-apps-macosmicrosoftedgeapp.md) no corpo da resposta.</span><span class="sxs-lookup"><span data-stu-id="62325-129">If successful, this method returns a `200 OK` response code and a collection of [macOSMicrosoftEdgeApp](../resources/intune-apps-macosmicrosoftedgeapp.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="62325-130">Exemplo</span><span class="sxs-lookup"><span data-stu-id="62325-130">Example</span></span>

### <a name="request"></a><span data-ttu-id="62325-131">Solicitação</span><span class="sxs-lookup"><span data-stu-id="62325-131">Request</span></span>
<span data-ttu-id="62325-132">Este é um exemplo da solicitação.</span><span class="sxs-lookup"><span data-stu-id="62325-132">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceAppManagement/mobileApps
```

### <a name="response"></a><span data-ttu-id="62325-133">Resposta</span><span class="sxs-lookup"><span data-stu-id="62325-133">Response</span></span>
<span data-ttu-id="62325-p102">Veja a seguir um exemplo da resposta. Observação: o objeto response mostrado aqui pode estar truncado por motivos de concisão. Todas as propriedades serão retornadas de uma chamada real.</span><span class="sxs-lookup"><span data-stu-id="62325-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1025

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.macOSMicrosoftEdgeApp",
      "id": "c964092a-092a-c964-2a09-64c92a0964c9",
      "displayName": "Display Name value",
      "description": "Description value",
      "publisher": "Publisher value",
      "largeIcon": {
        "@odata.type": "microsoft.graph.mimeContent",
        "type": "Type value",
        "value": "dmFsdWU="
      },
      "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
      "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
      "isFeatured": true,
      "privacyInformationUrl": "https://example.com/privacyInformationUrl/",
      "informationUrl": "https://example.com/informationUrl/",
      "owner": "Owner value",
      "developer": "Developer value",
      "notes": "Notes value",
      "uploadState": 11,
      "publishingState": "processing",
      "isAssigned": true,
      "roleScopeTagIds": [
        "Role Scope Tag Ids value"
      ],
      "dependentAppCount": 1
    }
  ]
}
```





