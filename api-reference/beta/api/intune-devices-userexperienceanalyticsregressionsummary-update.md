---
title: Atualizar userExperienceAnalyticsRegressionSummary
description: Atualiza as propriedades de um objeto userExperienceAnalyticsRegressionSummary.
author: rolyon
localization_priority: Normal
ms.prod: Intune
doc_type: apiPageType
ms.openlocfilehash: dcc7aab75801de94b292e5cac7bcb6d206b183a1
ms.sourcegitcommit: 0dcabe677927c259c2ddcefd0d5e2a2aef065e8b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/16/2019
ms.locfileid: "37529099"
---
# <a name="update-userexperienceanalyticsregressionsummary"></a><span data-ttu-id="48488-103">Atualizar userExperienceAnalyticsRegressionSummary</span><span class="sxs-lookup"><span data-stu-id="48488-103">Update userExperienceAnalyticsRegressionSummary</span></span>

> <span data-ttu-id="48488-104">**Importante:** As APIs do Microsoft Graph na versão/beta estão sujeitas a alterações; Não há suporte para o uso de produção.</span><span class="sxs-lookup"><span data-stu-id="48488-104">**Important:** Microsoft Graph APIs under the /beta version are subject to change; production use is not supported.</span></span>

> <span data-ttu-id="48488-105">**Observação:** A API do Microsoft Graph para Intune requer uma [licença do Active Intune](https://go.microsoft.com/fwlink/?linkid=839381) para o locatário.</span><span class="sxs-lookup"><span data-stu-id="48488-105">**Note:** The Microsoft Graph API for Intune requires an [active Intune license](https://go.microsoft.com/fwlink/?linkid=839381) for the tenant.</span></span>

<span data-ttu-id="48488-106">Atualiza as propriedades de um objeto [userExperienceAnalyticsRegressionSummary](../resources/intune-devices-userexperienceanalyticsregressionsummary.md) .</span><span class="sxs-lookup"><span data-stu-id="48488-106">Update the properties of a [userExperienceAnalyticsRegressionSummary](../resources/intune-devices-userexperienceanalyticsregressionsummary.md) object.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="48488-107">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="48488-107">Prerequisites</span></span>
<span data-ttu-id="48488-p101">Uma das seguintes permissões é obrigatória para chamar esta API. Para saber mais, incluindo como escolher permissões, confira [Permissões](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="48488-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="48488-110">Tipo de permissão</span><span class="sxs-lookup"><span data-stu-id="48488-110">Permission type</span></span>|<span data-ttu-id="48488-111">Permissões (de privilégios máximos a mínimos)</span><span class="sxs-lookup"><span data-stu-id="48488-111">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="48488-112">Delegado (conta corporativa ou de estudante)</span><span class="sxs-lookup"><span data-stu-id="48488-112">Delegated (work or school account)</span></span>|<span data-ttu-id="48488-113">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="48488-113">DeviceManagementManagedDevices.ReadWrite.All</span></span>|
|<span data-ttu-id="48488-114">Delegado (conta pessoal da Microsoft)</span><span class="sxs-lookup"><span data-stu-id="48488-114">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="48488-115">Sem suporte.</span><span class="sxs-lookup"><span data-stu-id="48488-115">Not supported.</span></span>|
|<span data-ttu-id="48488-116">Application</span><span class="sxs-lookup"><span data-stu-id="48488-116">Application</span></span>|<span data-ttu-id="48488-117">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="48488-117">DeviceManagementManagedDevices.ReadWrite.All</span></span>|

## <a name="http-request"></a><span data-ttu-id="48488-118">Solicitação HTTP</span><span class="sxs-lookup"><span data-stu-id="48488-118">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/userExperienceAnalyticsRegressionSummary
```

## <a name="request-headers"></a><span data-ttu-id="48488-119">Cabeçalhos de solicitação</span><span class="sxs-lookup"><span data-stu-id="48488-119">Request headers</span></span>
|<span data-ttu-id="48488-120">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="48488-120">Header</span></span>|<span data-ttu-id="48488-121">Valor</span><span class="sxs-lookup"><span data-stu-id="48488-121">Value</span></span>|
|:---|:---|
|<span data-ttu-id="48488-122">Autorização</span><span class="sxs-lookup"><span data-stu-id="48488-122">Authorization</span></span>|<span data-ttu-id="48488-123">&lt;Token&gt; de portador obrigatório.</span><span class="sxs-lookup"><span data-stu-id="48488-123">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="48488-124">Aceitar</span><span class="sxs-lookup"><span data-stu-id="48488-124">Accept</span></span>|<span data-ttu-id="48488-125">application/json</span><span class="sxs-lookup"><span data-stu-id="48488-125">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="48488-126">Corpo da solicitação</span><span class="sxs-lookup"><span data-stu-id="48488-126">Request body</span></span>
<span data-ttu-id="48488-127">No corpo da solicitação, forneça uma representação JSON do objeto [userExperienceAnalyticsRegressionSummary](../resources/intune-devices-userexperienceanalyticsregressionsummary.md) .</span><span class="sxs-lookup"><span data-stu-id="48488-127">In the request body, supply a JSON representation for the [userExperienceAnalyticsRegressionSummary](../resources/intune-devices-userexperienceanalyticsregressionsummary.md) object.</span></span>

<span data-ttu-id="48488-128">A tabela a seguir mostra as propriedades que são necessárias ao criar [userExperienceAnalyticsRegressionSummary](../resources/intune-devices-userexperienceanalyticsregressionsummary.md).</span><span class="sxs-lookup"><span data-stu-id="48488-128">The following table shows the properties that are required when you create the [userExperienceAnalyticsRegressionSummary](../resources/intune-devices-userexperienceanalyticsregressionsummary.md).</span></span>

|<span data-ttu-id="48488-129">Propriedade</span><span class="sxs-lookup"><span data-stu-id="48488-129">Property</span></span>|<span data-ttu-id="48488-130">Tipo</span><span class="sxs-lookup"><span data-stu-id="48488-130">Type</span></span>|<span data-ttu-id="48488-131">Descrição</span><span class="sxs-lookup"><span data-stu-id="48488-131">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="48488-132">id</span><span class="sxs-lookup"><span data-stu-id="48488-132">id</span></span>|<span data-ttu-id="48488-133">Cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="48488-133">String</span></span>|<span data-ttu-id="48488-134">O identificador exclusivo do Resumo de regressão da análise da experiência do usuário.</span><span class="sxs-lookup"><span data-stu-id="48488-134">The unique identifier of the user experience analytics regression summary.</span></span>|



## <a name="response"></a><span data-ttu-id="48488-135">Resposta</span><span class="sxs-lookup"><span data-stu-id="48488-135">Response</span></span>
<span data-ttu-id="48488-136">Se tiver êxito, este método retornará `200 OK` um código de resposta e um objeto [userExperienceAnalyticsRegressionSummary](../resources/intune-devices-userexperienceanalyticsregressionsummary.md) atualizado no corpo da resposta.</span><span class="sxs-lookup"><span data-stu-id="48488-136">If successful, this method returns a `200 OK` response code and an updated [userExperienceAnalyticsRegressionSummary](../resources/intune-devices-userexperienceanalyticsregressionsummary.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="48488-137">Exemplo</span><span class="sxs-lookup"><span data-stu-id="48488-137">Example</span></span>

### <a name="request"></a><span data-ttu-id="48488-138">Solicitação</span><span class="sxs-lookup"><span data-stu-id="48488-138">Request</span></span>
<span data-ttu-id="48488-139">Este é um exemplo da solicitação.</span><span class="sxs-lookup"><span data-stu-id="48488-139">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/userExperienceAnalyticsRegressionSummary
Content-type: application/json
Content-length: 82

{
  "@odata.type": "#microsoft.graph.userExperienceAnalyticsRegressionSummary"
}
```

### <a name="response"></a><span data-ttu-id="48488-140">Resposta</span><span class="sxs-lookup"><span data-stu-id="48488-140">Response</span></span>
<span data-ttu-id="48488-p102">Veja a seguir um exemplo da resposta. Observação: o objeto response mostrado aqui pode estar truncado por motivos de concisão. Todas as propriedades serão retornadas de uma chamada real.</span><span class="sxs-lookup"><span data-stu-id="48488-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 131

{
  "@odata.type": "#microsoft.graph.userExperienceAnalyticsRegressionSummary",
  "id": "41683327-3327-4168-2733-684127336841"
}
```





