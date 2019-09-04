---
title: Obter deviceManagementDerivedCredentialSettings
description: Leia as propriedades e as relações do objeto deviceManagementDerivedCredentialSettings.
author: rolyon
localization_priority: Normal
ms.prod: Intune
doc_type: apiPageType
ms.openlocfilehash: ce291c710792d15006543b9dc2c7f3db5051917b
ms.sourcegitcommit: 0f3e0bd7b57870a0f7b34cf52eaf4776ac82671e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/31/2019
ms.locfileid: "36699471"
---
# <a name="get-devicemanagementderivedcredentialsettings"></a><span data-ttu-id="10e41-103">Obter deviceManagementDerivedCredentialSettings</span><span class="sxs-lookup"><span data-stu-id="10e41-103">Get deviceManagementDerivedCredentialSettings</span></span>

> <span data-ttu-id="10e41-104">**Importante:** As APIs do Microsoft Graph na versão/beta estão sujeitas a alterações; Não há suporte para o uso de produção.</span><span class="sxs-lookup"><span data-stu-id="10e41-104">**Important:** Microsoft Graph APIs under the /beta version are subject to change; production use is not supported.</span></span>

> <span data-ttu-id="10e41-105">**Observação:** A API do Microsoft Graph para Intune requer uma [licença do Active Intune](https://go.microsoft.com/fwlink/?linkid=839381) para o locatário.</span><span class="sxs-lookup"><span data-stu-id="10e41-105">**Note:** The Microsoft Graph API for Intune requires an [active Intune license](https://go.microsoft.com/fwlink/?linkid=839381) for the tenant.</span></span>

<span data-ttu-id="10e41-106">Leia as propriedades e as relações do objeto [deviceManagementDerivedCredentialSettings](../resources/intune-shared-devicemanagementderivedcredentialsettings.md) .</span><span class="sxs-lookup"><span data-stu-id="10e41-106">Read properties and relationships of the [deviceManagementDerivedCredentialSettings](../resources/intune-shared-devicemanagementderivedcredentialsettings.md) object.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="10e41-107">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="10e41-107">Prerequisites</span></span>
<span data-ttu-id="10e41-p101">Uma das seguintes permissões é obrigatória para chamar esta API. Para saber mais, incluindo como escolher permissões, confira [Permissões](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="10e41-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="10e41-110">Tipo de permissão</span><span class="sxs-lookup"><span data-stu-id="10e41-110">Permission type</span></span>|<span data-ttu-id="10e41-111">Permissões (de privilégios máximos a mínimos)</span><span class="sxs-lookup"><span data-stu-id="10e41-111">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="10e41-112">Delegado (conta corporativa ou de estudante)</span><span class="sxs-lookup"><span data-stu-id="10e41-112">Delegated (work or school account)</span></span>||
|<span data-ttu-id="10e41-113">&nbsp; &nbsp; **Configuração do dispositivo**</span><span class="sxs-lookup"><span data-stu-id="10e41-113">&nbsp; &nbsp; **Device configuration**</span></span> | <span data-ttu-id="10e41-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="10e41-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="10e41-115">&nbsp;&nbsp; **Política de acesso de recursos**</span><span class="sxs-lookup"><span data-stu-id="10e41-115">&nbsp; &nbsp; **Resource Access Policy**</span></span> | <span data-ttu-id="10e41-116">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="10e41-116">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="10e41-117">Delegado (conta pessoal da Microsoft)</span><span class="sxs-lookup"><span data-stu-id="10e41-117">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="10e41-118">Sem suporte.</span><span class="sxs-lookup"><span data-stu-id="10e41-118">Not supported.</span></span>|
|<span data-ttu-id="10e41-119">Aplicativo</span><span class="sxs-lookup"><span data-stu-id="10e41-119">Application</span></span>||
|<span data-ttu-id="10e41-120">&nbsp; &nbsp; **Configuração do dispositivo**</span><span class="sxs-lookup"><span data-stu-id="10e41-120">&nbsp; &nbsp; **Device configuration**</span></span> | <span data-ttu-id="10e41-121">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="10e41-121">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="10e41-122">&nbsp;&nbsp; **Política de acesso de recursos**</span><span class="sxs-lookup"><span data-stu-id="10e41-122">&nbsp; &nbsp; **Resource Access Policy**</span></span> | <span data-ttu-id="10e41-123">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="10e41-123">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|

## <a name="http-request"></a><span data-ttu-id="10e41-124">Solicitação HTTP</span><span class="sxs-lookup"><span data-stu-id="10e41-124">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/derivedCredentials/{deviceManagementDerivedCredentialSettingsId}
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/derivedCredentialSettings
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.iosVpnConfiguration/derivedCredentialSettings
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.iosEnterpriseWiFiConfiguration/derivedCredentialSettings
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.iosEasEmailProfileConfiguration/derivedCredentialSettings
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.iosDerivedCredentialAuthenticationConfiguration/derivedCredentialSettings
```

## <a name="optional-query-parameters"></a><span data-ttu-id="10e41-125">Parâmetros de consulta opcionais</span><span class="sxs-lookup"><span data-stu-id="10e41-125">Optional query parameters</span></span>
<span data-ttu-id="10e41-126">Este método dá suporte a [Parâmetros de consulta OData](https://docs.microsoft.com/en-us/graph/query-parameters) para ajudar a personalizar a resposta.</span><span class="sxs-lookup"><span data-stu-id="10e41-126">This method supports the [OData Query Parameters](https://docs.microsoft.com/en-us/graph/query-parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="10e41-127">Cabeçalhos de solicitação</span><span class="sxs-lookup"><span data-stu-id="10e41-127">Request headers</span></span>
|<span data-ttu-id="10e41-128">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="10e41-128">Header</span></span>|<span data-ttu-id="10e41-129">Valor</span><span class="sxs-lookup"><span data-stu-id="10e41-129">Value</span></span>|
|:---|:---|
|<span data-ttu-id="10e41-130">Autorização</span><span class="sxs-lookup"><span data-stu-id="10e41-130">Authorization</span></span>|<span data-ttu-id="10e41-131">&lt;Token&gt; de portador obrigatório.</span><span class="sxs-lookup"><span data-stu-id="10e41-131">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="10e41-132">Aceitar</span><span class="sxs-lookup"><span data-stu-id="10e41-132">Accept</span></span>|<span data-ttu-id="10e41-133">application/json</span><span class="sxs-lookup"><span data-stu-id="10e41-133">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="10e41-134">Corpo da solicitação</span><span class="sxs-lookup"><span data-stu-id="10e41-134">Request body</span></span>
<span data-ttu-id="10e41-135">Não forneça um corpo de solicitação para esse método.</span><span class="sxs-lookup"><span data-stu-id="10e41-135">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="10e41-136">Resposta</span><span class="sxs-lookup"><span data-stu-id="10e41-136">Response</span></span>
<span data-ttu-id="10e41-137">Se bem-sucedido, este método retorna um `200 OK` código de resposta e um objeto [deviceManagementDerivedCredentialSettings](../resources/intune-shared-devicemanagementderivedcredentialsettings.md) no corpo da resposta.</span><span class="sxs-lookup"><span data-stu-id="10e41-137">If successful, this method returns a `200 OK` response code and [deviceManagementDerivedCredentialSettings](../resources/intune-shared-devicemanagementderivedcredentialsettings.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="10e41-138">Exemplo</span><span class="sxs-lookup"><span data-stu-id="10e41-138">Example</span></span>

### <a name="request"></a><span data-ttu-id="10e41-139">Solicitação</span><span class="sxs-lookup"><span data-stu-id="10e41-139">Request</span></span>
<span data-ttu-id="10e41-140">Este é um exemplo da solicitação.</span><span class="sxs-lookup"><span data-stu-id="10e41-140">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations/{deviceConfigurationId}/derivedCredentialSettings
```

### <a name="response"></a><span data-ttu-id="10e41-141">Resposta</span><span class="sxs-lookup"><span data-stu-id="10e41-141">Response</span></span>
<span data-ttu-id="10e41-p102">Veja a seguir um exemplo da resposta. Observação: o objeto response mostrado aqui pode estar truncado por motivos de concisão. Todas as propriedades serão retornadas de uma chamada real.</span><span class="sxs-lookup"><span data-stu-id="10e41-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 155

{
  "value": {
    "@odata.type": "#microsoft.graph.deviceManagementDerivedCredentialSettings",
    "id": "bc650741-0741-bc65-4107-65bc410765bc"
  }
}
