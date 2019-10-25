---
title: Atualizar deviceManagementReportSchedule
description: Atualiza as propriedades de um objeto deviceManagementReportSchedule.
author: rolyon
localization_priority: Normal
ms.prod: Intune
doc_type: apiPageType
ms.openlocfilehash: f46c8881e1b936f224bd6a4f5c493f0fd69bb997
ms.sourcegitcommit: 0dcabe677927c259c2ddcefd0d5e2a2aef065e8b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/16/2019
ms.locfileid: "37537167"
---
# <a name="update-devicemanagementreportschedule"></a><span data-ttu-id="23317-103">Atualizar deviceManagementReportSchedule</span><span class="sxs-lookup"><span data-stu-id="23317-103">Update deviceManagementReportSchedule</span></span>

> <span data-ttu-id="23317-104">**Importante:** As APIs do Microsoft Graph na versão/beta estão sujeitas a alterações; Não há suporte para o uso de produção.</span><span class="sxs-lookup"><span data-stu-id="23317-104">**Important:** Microsoft Graph APIs under the /beta version are subject to change; production use is not supported.</span></span>

> <span data-ttu-id="23317-105">**Observação:** A API do Microsoft Graph para Intune requer uma [licença do Active Intune](https://go.microsoft.com/fwlink/?linkid=839381) para o locatário.</span><span class="sxs-lookup"><span data-stu-id="23317-105">**Note:** The Microsoft Graph API for Intune requires an [active Intune license](https://go.microsoft.com/fwlink/?linkid=839381) for the tenant.</span></span>

<span data-ttu-id="23317-106">Atualiza as propriedades de um objeto [deviceManagementReportSchedule](../resources/intune-reporting-devicemanagementreportschedule.md) .</span><span class="sxs-lookup"><span data-stu-id="23317-106">Update the properties of a [deviceManagementReportSchedule](../resources/intune-reporting-devicemanagementreportschedule.md) object.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="23317-107">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="23317-107">Prerequisites</span></span>
<span data-ttu-id="23317-p101">Uma das seguintes permissões é obrigatória para chamar esta API. Para saber mais, incluindo como escolher permissões, confira [Permissões](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="23317-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="23317-110">Tipo de permissão</span><span class="sxs-lookup"><span data-stu-id="23317-110">Permission type</span></span>|<span data-ttu-id="23317-111">Permissões (de privilégios máximos a mínimos)</span><span class="sxs-lookup"><span data-stu-id="23317-111">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="23317-112">Delegado (conta corporativa ou de estudante)</span><span class="sxs-lookup"><span data-stu-id="23317-112">Delegated (work or school account)</span></span>|<span data-ttu-id="23317-113">DeviceManagementConfiguration. ReadWrite. All, DeviceManagementApps. ReadWrite. All, DeviceManagementManagedDevices. ReadWrite. All</span><span class="sxs-lookup"><span data-stu-id="23317-113">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementApps.ReadWrite.All, DeviceManagementManagedDevices.ReadWrite.All</span></span>|
|<span data-ttu-id="23317-114">Delegado (conta pessoal da Microsoft)</span><span class="sxs-lookup"><span data-stu-id="23317-114">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="23317-115">Sem suporte.</span><span class="sxs-lookup"><span data-stu-id="23317-115">Not supported.</span></span>|
|<span data-ttu-id="23317-116">Application</span><span class="sxs-lookup"><span data-stu-id="23317-116">Application</span></span>|<span data-ttu-id="23317-117">DeviceManagementConfiguration. ReadWrite. All, DeviceManagementApps. ReadWrite. All, DeviceManagementManagedDevices. ReadWrite. All</span><span class="sxs-lookup"><span data-stu-id="23317-117">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementApps.ReadWrite.All, DeviceManagementManagedDevices.ReadWrite.All</span></span>|

## <a name="http-request"></a><span data-ttu-id="23317-118">Solicitação HTTP</span><span class="sxs-lookup"><span data-stu-id="23317-118">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/reports/reportSchedules/{deviceManagementReportScheduleId}
```

## <a name="request-headers"></a><span data-ttu-id="23317-119">Cabeçalhos de solicitação</span><span class="sxs-lookup"><span data-stu-id="23317-119">Request headers</span></span>
|<span data-ttu-id="23317-120">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="23317-120">Header</span></span>|<span data-ttu-id="23317-121">Valor</span><span class="sxs-lookup"><span data-stu-id="23317-121">Value</span></span>|
|:---|:---|
|<span data-ttu-id="23317-122">Autorização</span><span class="sxs-lookup"><span data-stu-id="23317-122">Authorization</span></span>|<span data-ttu-id="23317-123">&lt;Token&gt; de portador obrigatório.</span><span class="sxs-lookup"><span data-stu-id="23317-123">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="23317-124">Aceitar</span><span class="sxs-lookup"><span data-stu-id="23317-124">Accept</span></span>|<span data-ttu-id="23317-125">application/json</span><span class="sxs-lookup"><span data-stu-id="23317-125">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="23317-126">Corpo da solicitação</span><span class="sxs-lookup"><span data-stu-id="23317-126">Request body</span></span>
<span data-ttu-id="23317-127">No corpo da solicitação, forneça uma representação JSON do objeto [deviceManagementReportSchedule](../resources/intune-reporting-devicemanagementreportschedule.md) .</span><span class="sxs-lookup"><span data-stu-id="23317-127">In the request body, supply a JSON representation for the [deviceManagementReportSchedule](../resources/intune-reporting-devicemanagementreportschedule.md) object.</span></span>

<span data-ttu-id="23317-128">A tabela a seguir mostra as propriedades que são necessárias ao criar [deviceManagementReportSchedule](../resources/intune-reporting-devicemanagementreportschedule.md).</span><span class="sxs-lookup"><span data-stu-id="23317-128">The following table shows the properties that are required when you create the [deviceManagementReportSchedule](../resources/intune-reporting-devicemanagementreportschedule.md).</span></span>

|<span data-ttu-id="23317-129">Propriedade</span><span class="sxs-lookup"><span data-stu-id="23317-129">Property</span></span>|<span data-ttu-id="23317-130">Tipo</span><span class="sxs-lookup"><span data-stu-id="23317-130">Type</span></span>|<span data-ttu-id="23317-131">Descrição</span><span class="sxs-lookup"><span data-stu-id="23317-131">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="23317-132">id</span><span class="sxs-lookup"><span data-stu-id="23317-132">id</span></span>|<span data-ttu-id="23317-133">String</span><span class="sxs-lookup"><span data-stu-id="23317-133">String</span></span>|<span data-ttu-id="23317-134">Identificador exclusivo para esta entidade</span><span class="sxs-lookup"><span data-stu-id="23317-134">Unique identifier for this entity</span></span>|
|<span data-ttu-id="23317-135">reportScheduleName</span><span class="sxs-lookup"><span data-stu-id="23317-135">reportScheduleName</span></span>|<span data-ttu-id="23317-136">Cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="23317-136">String</span></span>|<span data-ttu-id="23317-137">Nome da agenda</span><span class="sxs-lookup"><span data-stu-id="23317-137">Name of the schedule</span></span>|
|<span data-ttu-id="23317-138">subject</span><span class="sxs-lookup"><span data-stu-id="23317-138">subject</span></span>|<span data-ttu-id="23317-139">String</span><span class="sxs-lookup"><span data-stu-id="23317-139">String</span></span>|<span data-ttu-id="23317-140">Assunto dos relatórios agendados que são entregues</span><span class="sxs-lookup"><span data-stu-id="23317-140">Subject of the scheduled reports that are delivered</span></span>|
|<span data-ttu-id="23317-141">email</span><span class="sxs-lookup"><span data-stu-id="23317-141">emails</span></span>|<span data-ttu-id="23317-142">String collection</span><span class="sxs-lookup"><span data-stu-id="23317-142">String collection</span></span>|<span data-ttu-id="23317-143">Emails para os quais os relatórios agendados são entregues</span><span class="sxs-lookup"><span data-stu-id="23317-143">Emails to which the scheduled reports are delivered</span></span>|
|<span data-ttu-id="23317-144">recurrence</span><span class="sxs-lookup"><span data-stu-id="23317-144">recurrence</span></span>|[<span data-ttu-id="23317-145">deviceManagementScheduledReportRecurrence</span><span class="sxs-lookup"><span data-stu-id="23317-145">deviceManagementScheduledReportRecurrence</span></span>](../resources/intune-reporting-devicemanagementscheduledreportrecurrence.md)|<span data-ttu-id="23317-146">Frequência da entrega de relatórios agendados.</span><span class="sxs-lookup"><span data-stu-id="23317-146">Frequency of scheduled report delivery.</span></span> <span data-ttu-id="23317-147">Os valores possíveis são: `none`, `daily`, `weekly`, `monthly`.</span><span class="sxs-lookup"><span data-stu-id="23317-147">Possible values are: `none`, `daily`, `weekly`, `monthly`.</span></span>|
|<span data-ttu-id="23317-148">startDateTime</span><span class="sxs-lookup"><span data-stu-id="23317-148">startDateTime</span></span>|<span data-ttu-id="23317-149">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="23317-149">DateTimeOffset</span></span>|<span data-ttu-id="23317-150">Hora de início da entrega dos relatórios agendados</span><span class="sxs-lookup"><span data-stu-id="23317-150">Time that the delivery of the scheduled reports starts</span></span>|
|<span data-ttu-id="23317-151">endDateTime</span><span class="sxs-lookup"><span data-stu-id="23317-151">endDateTime</span></span>|<span data-ttu-id="23317-152">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="23317-152">DateTimeOffset</span></span>|<span data-ttu-id="23317-153">Hora em que a entrega dos relatórios agendados termina</span><span class="sxs-lookup"><span data-stu-id="23317-153">Time that the delivery of the scheduled reports ends</span></span>|
|<span data-ttu-id="23317-154">userId</span><span class="sxs-lookup"><span data-stu-id="23317-154">userId</span></span>|<span data-ttu-id="23317-155">Cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="23317-155">String</span></span>|<span data-ttu-id="23317-156">A ID do usuário que criou o relatório</span><span class="sxs-lookup"><span data-stu-id="23317-156">The Id of the User who created the report</span></span>|
|<span data-ttu-id="23317-157">reportName</span><span class="sxs-lookup"><span data-stu-id="23317-157">reportName</span></span>|<span data-ttu-id="23317-158">Cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="23317-158">String</span></span>|<span data-ttu-id="23317-159">Nome do relatório</span><span class="sxs-lookup"><span data-stu-id="23317-159">Name of the report</span></span>|
|<span data-ttu-id="23317-160">filter</span><span class="sxs-lookup"><span data-stu-id="23317-160">filter</span></span>|<span data-ttu-id="23317-161">Cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="23317-161">String</span></span>|<span data-ttu-id="23317-162">Filtros aplicados no relatório</span><span class="sxs-lookup"><span data-stu-id="23317-162">Filters applied on the report</span></span>|
|<span data-ttu-id="23317-163">select</span><span class="sxs-lookup"><span data-stu-id="23317-163">select</span></span>|<span data-ttu-id="23317-164">String collection</span><span class="sxs-lookup"><span data-stu-id="23317-164">String collection</span></span>|<span data-ttu-id="23317-165">Colunas selecionadas do relatório</span><span class="sxs-lookup"><span data-stu-id="23317-165">Columns selected from the report</span></span>|
|<span data-ttu-id="23317-166">Classificadoporativado</span><span class="sxs-lookup"><span data-stu-id="23317-166">orderBy</span></span>|<span data-ttu-id="23317-167">String collection</span><span class="sxs-lookup"><span data-stu-id="23317-167">String collection</span></span>|<span data-ttu-id="23317-168">Ordenação de colunas no relatório</span><span class="sxs-lookup"><span data-stu-id="23317-168">Ordering of columns in the report</span></span>|
|<span data-ttu-id="23317-169">formato</span><span class="sxs-lookup"><span data-stu-id="23317-169">format</span></span>|[<span data-ttu-id="23317-170">deviceManagementReportFileFormat</span><span class="sxs-lookup"><span data-stu-id="23317-170">deviceManagementReportFileFormat</span></span>](../resources/intune-reporting-devicemanagementreportfileformat.md)|<span data-ttu-id="23317-171">Formato do relatório agendado.</span><span class="sxs-lookup"><span data-stu-id="23317-171">Format of the scheduled report.</span></span> <span data-ttu-id="23317-172">Os valores possíveis são: `csv` e `pdf`.</span><span class="sxs-lookup"><span data-stu-id="23317-172">Possible values are: `csv`, `pdf`.</span></span>|



## <a name="response"></a><span data-ttu-id="23317-173">Resposta</span><span class="sxs-lookup"><span data-stu-id="23317-173">Response</span></span>
<span data-ttu-id="23317-174">Se tiver êxito, este método retornará `200 OK` um código de resposta e um objeto [deviceManagementReportSchedule](../resources/intune-reporting-devicemanagementreportschedule.md) atualizado no corpo da resposta.</span><span class="sxs-lookup"><span data-stu-id="23317-174">If successful, this method returns a `200 OK` response code and an updated [deviceManagementReportSchedule](../resources/intune-reporting-devicemanagementreportschedule.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="23317-175">Exemplo</span><span class="sxs-lookup"><span data-stu-id="23317-175">Example</span></span>

### <a name="request"></a><span data-ttu-id="23317-176">Solicitação</span><span class="sxs-lookup"><span data-stu-id="23317-176">Request</span></span>
<span data-ttu-id="23317-177">Este é um exemplo da solicitação.</span><span class="sxs-lookup"><span data-stu-id="23317-177">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/reports/reportSchedules/{deviceManagementReportScheduleId}
Content-type: application/json
Content-length: 539

{
  "@odata.type": "#microsoft.graph.deviceManagementReportSchedule",
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
```

### <a name="response"></a><span data-ttu-id="23317-178">Resposta</span><span class="sxs-lookup"><span data-stu-id="23317-178">Response</span></span>
<span data-ttu-id="23317-p104">Veja a seguir um exemplo da resposta. Observação: o objeto response mostrado aqui pode estar truncado por motivos de concisão. Todas as propriedades serão retornadas de uma chamada real.</span><span class="sxs-lookup"><span data-stu-id="23317-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 588

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
```





