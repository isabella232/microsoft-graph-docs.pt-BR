---
title: Atualizar macManagedAppProtection
description: Atualiza as propriedades de um objeto macManagedAppProtection.
author: rolyon
localization_priority: Normal
ms.prod: Intune
doc_type: apiPageType
ms.openlocfilehash: 2b0f156b004e612c26babd0b24f659c1a1c226f3
ms.sourcegitcommit: 86903a4730bbd825eabb7f0a1b2429723cc8b1e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/26/2019
ms.locfileid: "37191787"
---
# <a name="update-macmanagedappprotection"></a><span data-ttu-id="542e1-103">Atualizar macManagedAppProtection</span><span class="sxs-lookup"><span data-stu-id="542e1-103">Update macManagedAppProtection</span></span>

> <span data-ttu-id="542e1-104">**Importante:** As APIs do Microsoft Graph na versão/beta estão sujeitas a alterações; Não há suporte para o uso de produção.</span><span class="sxs-lookup"><span data-stu-id="542e1-104">**Important:** Microsoft Graph APIs under the /beta version are subject to change; production use is not supported.</span></span>

> <span data-ttu-id="542e1-105">**Observação:** A API do Microsoft Graph para Intune requer uma [licença do Active Intune](https://go.microsoft.com/fwlink/?linkid=839381) para o locatário.</span><span class="sxs-lookup"><span data-stu-id="542e1-105">**Note:** The Microsoft Graph API for Intune requires an [active Intune license](https://go.microsoft.com/fwlink/?linkid=839381) for the tenant.</span></span>

<span data-ttu-id="542e1-106">Atualiza as propriedades de um objeto [macManagedAppProtection](../resources/intune-policyset-macmanagedappprotection.md) .</span><span class="sxs-lookup"><span data-stu-id="542e1-106">Update the properties of a [macManagedAppProtection](../resources/intune-policyset-macmanagedappprotection.md) object.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="542e1-107">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="542e1-107">Prerequisites</span></span>
<span data-ttu-id="542e1-p101">Uma das seguintes permissões é obrigatória para chamar esta API. Para saber mais, incluindo como escolher permissões, confira [Permissões](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="542e1-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="542e1-110">Tipo de permissão</span><span class="sxs-lookup"><span data-stu-id="542e1-110">Permission type</span></span>|<span data-ttu-id="542e1-111">Permissões (de privilégios máximos a mínimos)</span><span class="sxs-lookup"><span data-stu-id="542e1-111">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="542e1-112">Delegado (conta corporativa ou de estudante)</span><span class="sxs-lookup"><span data-stu-id="542e1-112">Delegated (work or school account)</span></span>|<span data-ttu-id="542e1-113">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="542e1-113">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="542e1-114">Delegado (conta pessoal da Microsoft)</span><span class="sxs-lookup"><span data-stu-id="542e1-114">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="542e1-115">Sem suporte.</span><span class="sxs-lookup"><span data-stu-id="542e1-115">Not supported.</span></span>|
|<span data-ttu-id="542e1-116">Aplicativo</span><span class="sxs-lookup"><span data-stu-id="542e1-116">Application</span></span>|<span data-ttu-id="542e1-117">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="542e1-117">DeviceManagementApps.ReadWrite.All</span></span>|

## <a name="http-request"></a><span data-ttu-id="542e1-118">Solicitação HTTP</span><span class="sxs-lookup"><span data-stu-id="542e1-118">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/macManagedAppProtections/{macManagedAppProtectionId}
```

## <a name="request-headers"></a><span data-ttu-id="542e1-119">Cabeçalhos de solicitação</span><span class="sxs-lookup"><span data-stu-id="542e1-119">Request headers</span></span>
|<span data-ttu-id="542e1-120">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="542e1-120">Header</span></span>|<span data-ttu-id="542e1-121">Valor</span><span class="sxs-lookup"><span data-stu-id="542e1-121">Value</span></span>|
|:---|:---|
|<span data-ttu-id="542e1-122">Autorização</span><span class="sxs-lookup"><span data-stu-id="542e1-122">Authorization</span></span>|<span data-ttu-id="542e1-123">&lt;Token&gt; de portador obrigatório.</span><span class="sxs-lookup"><span data-stu-id="542e1-123">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="542e1-124">Aceitar</span><span class="sxs-lookup"><span data-stu-id="542e1-124">Accept</span></span>|<span data-ttu-id="542e1-125">application/json</span><span class="sxs-lookup"><span data-stu-id="542e1-125">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="542e1-126">Corpo da solicitação</span><span class="sxs-lookup"><span data-stu-id="542e1-126">Request body</span></span>
<span data-ttu-id="542e1-127">No corpo da solicitação, forneça uma representação JSON do objeto [macManagedAppProtection](../resources/intune-policyset-macmanagedappprotection.md) .</span><span class="sxs-lookup"><span data-stu-id="542e1-127">In the request body, supply a JSON representation for the [macManagedAppProtection](../resources/intune-policyset-macmanagedappprotection.md) object.</span></span>

<span data-ttu-id="542e1-128">A tabela a seguir mostra as propriedades que são necessárias ao criar [macManagedAppProtection](../resources/intune-policyset-macmanagedappprotection.md).</span><span class="sxs-lookup"><span data-stu-id="542e1-128">The following table shows the properties that are required when you create the [macManagedAppProtection](../resources/intune-policyset-macmanagedappprotection.md).</span></span>

|<span data-ttu-id="542e1-129">Propriedade</span><span class="sxs-lookup"><span data-stu-id="542e1-129">Property</span></span>|<span data-ttu-id="542e1-130">Tipo</span><span class="sxs-lookup"><span data-stu-id="542e1-130">Type</span></span>|<span data-ttu-id="542e1-131">Descrição</span><span class="sxs-lookup"><span data-stu-id="542e1-131">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="542e1-132">id</span><span class="sxs-lookup"><span data-stu-id="542e1-132">id</span></span>|<span data-ttu-id="542e1-133">String</span><span class="sxs-lookup"><span data-stu-id="542e1-133">String</span></span>|<span data-ttu-id="542e1-134">Ainda não documentado</span><span class="sxs-lookup"><span data-stu-id="542e1-134">Not yet documented</span></span>|



## <a name="response"></a><span data-ttu-id="542e1-135">Resposta</span><span class="sxs-lookup"><span data-stu-id="542e1-135">Response</span></span>
<span data-ttu-id="542e1-136">Se tiver êxito, este método retornará `200 OK` um código de resposta e um objeto [macManagedAppProtection](../resources/intune-policyset-macmanagedappprotection.md) atualizado no corpo da resposta.</span><span class="sxs-lookup"><span data-stu-id="542e1-136">If successful, this method returns a `200 OK` response code and an updated [macManagedAppProtection](../resources/intune-policyset-macmanagedappprotection.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="542e1-137">Exemplo</span><span class="sxs-lookup"><span data-stu-id="542e1-137">Example</span></span>

### <a name="request"></a><span data-ttu-id="542e1-138">Solicitação</span><span class="sxs-lookup"><span data-stu-id="542e1-138">Request</span></span>
<span data-ttu-id="542e1-139">Este é um exemplo da solicitação.</span><span class="sxs-lookup"><span data-stu-id="542e1-139">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceAppManagement/macManagedAppProtections/{macManagedAppProtectionId}
Content-type: application/json
Content-length: 65

{
  "@odata.type": "#microsoft.graph.macManagedAppProtection"
}
```

### <a name="response"></a><span data-ttu-id="542e1-140">Resposta</span><span class="sxs-lookup"><span data-stu-id="542e1-140">Response</span></span>
<span data-ttu-id="542e1-p102">Veja a seguir um exemplo da resposta. Observação: o objeto response mostrado aqui pode estar truncado por motivos de concisão. Todas as propriedades serão retornadas de uma chamada real.</span><span class="sxs-lookup"><span data-stu-id="542e1-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 114

{
  "@odata.type": "#microsoft.graph.macManagedAppProtection",
  "id": "bb139531-9531-bb13-3195-13bb319513bb"
}
```



