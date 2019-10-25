---
title: Listar deviceManagementReportSchedules
description: Listar Propriedades e relações dos objetos deviceManagementReportSchedule.
author: rolyon
localization_priority: Normal
ms.prod: Intune
doc_type: apiPageType
ms.openlocfilehash: e8e0f34e30c9ab23ad949a453252c11264d9ffd9
ms.sourcegitcommit: 0dcabe677927c259c2ddcefd0d5e2a2aef065e8b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/16/2019
ms.locfileid: "37537174"
---
# <a name="list-devicemanagementreportschedules"></a><span data-ttu-id="39594-103">Listar deviceManagementReportSchedules</span><span class="sxs-lookup"><span data-stu-id="39594-103">List deviceManagementReportSchedules</span></span>

> <span data-ttu-id="39594-104">**Importante:** As APIs do Microsoft Graph na versão/beta estão sujeitas a alterações; Não há suporte para o uso de produção.</span><span class="sxs-lookup"><span data-stu-id="39594-104">**Important:** Microsoft Graph APIs under the /beta version are subject to change; production use is not supported.</span></span>

> <span data-ttu-id="39594-105">**Observação:** A API do Microsoft Graph para Intune requer uma [licença do Active Intune](https://go.microsoft.com/fwlink/?linkid=839381) para o locatário.</span><span class="sxs-lookup"><span data-stu-id="39594-105">**Note:** The Microsoft Graph API for Intune requires an [active Intune license](https://go.microsoft.com/fwlink/?linkid=839381) for the tenant.</span></span>

<span data-ttu-id="39594-106">Listar Propriedades e relações dos objetos [deviceManagementReportSchedule](../resources/intune-reporting-devicemanagementreportschedule.md) .</span><span class="sxs-lookup"><span data-stu-id="39594-106">List properties and relationships of the [deviceManagementReportSchedule](../resources/intune-reporting-devicemanagementreportschedule.md) objects.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="39594-107">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="39594-107">Prerequisites</span></span>
<span data-ttu-id="39594-p101">Uma das seguintes permissões é obrigatória para chamar esta API. Para saber mais, incluindo como escolher permissões, confira [Permissões](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="39594-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="39594-110">Tipo de permissão</span><span class="sxs-lookup"><span data-stu-id="39594-110">Permission type</span></span>|<span data-ttu-id="39594-111">Permissões (de privilégios máximos a mínimos)</span><span class="sxs-lookup"><span data-stu-id="39594-111">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="39594-112">Delegado (conta corporativa ou de estudante)</span><span class="sxs-lookup"><span data-stu-id="39594-112">Delegated (work or school account)</span></span>|<span data-ttu-id="39594-113">DeviceManagementConfiguration. ReadWrite. All, DeviceManagementConfiguration. Read. All, DeviceManagementApps. ReadWrite. All, DeviceManagementApps. Read. All, DeviceManagementManagedDevices. ReadWrite. All, DeviceManagementManagedDevices. Read. All</span><span class="sxs-lookup"><span data-stu-id="39594-113">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All, DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All, DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span></span>|
|<span data-ttu-id="39594-114">Delegado (conta pessoal da Microsoft)</span><span class="sxs-lookup"><span data-stu-id="39594-114">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="39594-115">Sem suporte.</span><span class="sxs-lookup"><span data-stu-id="39594-115">Not supported.</span></span>|
|<span data-ttu-id="39594-116">Application</span><span class="sxs-lookup"><span data-stu-id="39594-116">Application</span></span>|<span data-ttu-id="39594-117">DeviceManagementConfiguration. ReadWrite. All, DeviceManagementConfiguration. Read. All, DeviceManagementApps. ReadWrite. All, DeviceManagementApps. Read. All, DeviceManagementManagedDevices. ReadWrite. All, DeviceManagementManagedDevices. Read. All</span><span class="sxs-lookup"><span data-stu-id="39594-117">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All, DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All, DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span></span>|

## <a name="http-request"></a><span data-ttu-id="39594-118">Solicitação HTTP</span><span class="sxs-lookup"><span data-stu-id="39594-118">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/reports/reportSchedules
```

## <a name="request-headers"></a><span data-ttu-id="39594-119">Cabeçalhos de solicitação</span><span class="sxs-lookup"><span data-stu-id="39594-119">Request headers</span></span>
|<span data-ttu-id="39594-120">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="39594-120">Header</span></span>|<span data-ttu-id="39594-121">Valor</span><span class="sxs-lookup"><span data-stu-id="39594-121">Value</span></span>|
|:---|:---|
|<span data-ttu-id="39594-122">Autorização</span><span class="sxs-lookup"><span data-stu-id="39594-122">Authorization</span></span>|<span data-ttu-id="39594-123">&lt;Token&gt; de portador obrigatório.</span><span class="sxs-lookup"><span data-stu-id="39594-123">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="39594-124">Aceitar</span><span class="sxs-lookup"><span data-stu-id="39594-124">Accept</span></span>|<span data-ttu-id="39594-125">application/json</span><span class="sxs-lookup"><span data-stu-id="39594-125">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="39594-126">Corpo da solicitação</span><span class="sxs-lookup"><span data-stu-id="39594-126">Request body</span></span>
<span data-ttu-id="39594-127">Não forneça um corpo de solicitação para esse método.</span><span class="sxs-lookup"><span data-stu-id="39594-127">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="39594-128">Resposta</span><span class="sxs-lookup"><span data-stu-id="39594-128">Response</span></span>
<span data-ttu-id="39594-129">Se tiver êxito, este método retornará `200 OK` um código de resposta e uma coleção de objetos [deviceManagementReportSchedule](../resources/intune-reporting-devicemanagementreportschedule.md) no corpo da resposta.</span><span class="sxs-lookup"><span data-stu-id="39594-129">If successful, this method returns a `200 OK` response code and a collection of [deviceManagementReportSchedule](../resources/intune-reporting-devicemanagementreportschedule.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="39594-130">Exemplo</span><span class="sxs-lookup"><span data-stu-id="39594-130">Example</span></span>

### <a name="request"></a><span data-ttu-id="39594-131">Solicitação</span><span class="sxs-lookup"><span data-stu-id="39594-131">Request</span></span>
<span data-ttu-id="39594-132">Este é um exemplo da solicitação.</span><span class="sxs-lookup"><span data-stu-id="39594-132">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/reports/reportSchedules
```

### <a name="response"></a><span data-ttu-id="39594-133">Resposta</span><span class="sxs-lookup"><span data-stu-id="39594-133">Response</span></span>
<span data-ttu-id="39594-p102">Veja a seguir um exemplo da resposta. Observação: o objeto response mostrado aqui pode estar truncado por motivos de concisão. Todas as propriedades serão retornadas de uma chamada real.</span><span class="sxs-lookup"><span data-stu-id="39594-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 701

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.deviceManagementReportSchedule",
      "id": "00bb9785-9785-00bb-8597-bb008597bb00",
      "reportScheduleName": "Report Schedule Name value",
      "subject": "Subject value",
      "emails": [
        "Emails value"
      ],
      "recurrence": "daily",
      "startDateTime": "2016-12-31T23:58:46.7156189-08:00",
      "endDateTime": "2017-01-01T00:03:30.9241974-08:00",
      "userId": "User Id value",
      "reportName": "Report Name value",
      "filter": "Filter value",
      "select": [
        "Select value"
      ],
      "orderBy": [
        "Order By value"
      ],
      "format": "pdf"
    }
  ]
}
```





