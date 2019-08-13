---
title: Atualizar androidDeviceOwnerVpnConfiguration
description: Atualiza as propriedades de um objeto androidDeviceOwnerVpnConfiguration.
author: rolyon
localization_priority: Normal
ms.prod: Intune
doc_type: apiPageType
ms.openlocfilehash: c8146d3813c94c3ef3c6a481d7dbc80c6c03598c
ms.sourcegitcommit: b5425ebf648572569b032ded5b56e1dcf3830515
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/13/2019
ms.locfileid: "36316847"
---
# <a name="update-androiddeviceownervpnconfiguration"></a><span data-ttu-id="2322c-103">Atualizar androidDeviceOwnerVpnConfiguration</span><span class="sxs-lookup"><span data-stu-id="2322c-103">Update androidDeviceOwnerVpnConfiguration</span></span>

> <span data-ttu-id="2322c-104">**Importante:** As APIs do Microsoft Graph na versão/beta estão sujeitas a alterações; Não há suporte para o uso de produção.</span><span class="sxs-lookup"><span data-stu-id="2322c-104">**Important:** Microsoft Graph APIs under the /beta version are subject to change; production use is not supported.</span></span>

> <span data-ttu-id="2322c-105">**Observação:** A API do Microsoft Graph para Intune requer uma [licença do Active Intune](https://go.microsoft.com/fwlink/?linkid=839381) para o locatário.</span><span class="sxs-lookup"><span data-stu-id="2322c-105">**Note:** The Microsoft Graph API for Intune requires an [active Intune license](https://go.microsoft.com/fwlink/?linkid=839381) for the tenant.</span></span>

<span data-ttu-id="2322c-106">Atualiza as propriedades de um objeto [androidDeviceOwnerVpnConfiguration](../resources/intune-deviceconfig-androiddeviceownervpnconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="2322c-106">Update the properties of a [androidDeviceOwnerVpnConfiguration](../resources/intune-deviceconfig-androiddeviceownervpnconfiguration.md) object.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="2322c-107">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="2322c-107">Prerequisites</span></span>
<span data-ttu-id="2322c-p101">Uma das seguintes permissões é obrigatória para chamar esta API. Para saber mais, incluindo como escolher permissões, confira [Permissões](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="2322c-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="2322c-110">Tipo de permissão</span><span class="sxs-lookup"><span data-stu-id="2322c-110">Permission type</span></span>|<span data-ttu-id="2322c-111">Permissões (de privilégios máximos a mínimos)</span><span class="sxs-lookup"><span data-stu-id="2322c-111">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="2322c-112">Delegado (conta corporativa ou de estudante)</span><span class="sxs-lookup"><span data-stu-id="2322c-112">Delegated (work or school account)</span></span>|<span data-ttu-id="2322c-113">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="2322c-113">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="2322c-114">Delegado (conta pessoal da Microsoft)</span><span class="sxs-lookup"><span data-stu-id="2322c-114">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="2322c-115">Sem suporte.</span><span class="sxs-lookup"><span data-stu-id="2322c-115">Not supported.</span></span>|
|<span data-ttu-id="2322c-116">Aplicativo</span><span class="sxs-lookup"><span data-stu-id="2322c-116">Application</span></span>|<span data-ttu-id="2322c-117">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="2322c-117">DeviceManagementConfiguration.ReadWrite.All</span></span>|

## <a name="http-request"></a><span data-ttu-id="2322c-118">Solicitação HTTP</span><span class="sxs-lookup"><span data-stu-id="2322c-118">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/groupAssignments/{deviceConfigurationGroupAssignmentId}/deviceConfiguration
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations/{deviceConfigurationId}
```

## <a name="request-headers"></a><span data-ttu-id="2322c-119">Cabeçalhos de solicitação</span><span class="sxs-lookup"><span data-stu-id="2322c-119">Request headers</span></span>
|<span data-ttu-id="2322c-120">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="2322c-120">Header</span></span>|<span data-ttu-id="2322c-121">Valor</span><span class="sxs-lookup"><span data-stu-id="2322c-121">Value</span></span>|
|:---|:---|
|<span data-ttu-id="2322c-122">Autorização</span><span class="sxs-lookup"><span data-stu-id="2322c-122">Authorization</span></span>|<span data-ttu-id="2322c-123">&lt;Token&gt; de portador obrigatório.</span><span class="sxs-lookup"><span data-stu-id="2322c-123">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="2322c-124">Aceitar</span><span class="sxs-lookup"><span data-stu-id="2322c-124">Accept</span></span>|<span data-ttu-id="2322c-125">application/json</span><span class="sxs-lookup"><span data-stu-id="2322c-125">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="2322c-126">Corpo da solicitação</span><span class="sxs-lookup"><span data-stu-id="2322c-126">Request body</span></span>
<span data-ttu-id="2322c-127">No corpo da solicitação, forneça uma representação JSON do objeto [androidDeviceOwnerVpnConfiguration](../resources/intune-deviceconfig-androiddeviceownervpnconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="2322c-127">In the request body, supply a JSON representation for the [androidDeviceOwnerVpnConfiguration](../resources/intune-deviceconfig-androiddeviceownervpnconfiguration.md) object.</span></span>

<span data-ttu-id="2322c-128">A tabela a seguir mostra as propriedades que são necessárias ao criar [androidDeviceOwnerVpnConfiguration](../resources/intune-deviceconfig-androiddeviceownervpnconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="2322c-128">The following table shows the properties that are required when you create the [androidDeviceOwnerVpnConfiguration](../resources/intune-deviceconfig-androiddeviceownervpnconfiguration.md).</span></span>

|<span data-ttu-id="2322c-129">Propriedade</span><span class="sxs-lookup"><span data-stu-id="2322c-129">Property</span></span>|<span data-ttu-id="2322c-130">Tipo</span><span class="sxs-lookup"><span data-stu-id="2322c-130">Type</span></span>|<span data-ttu-id="2322c-131">Descrição</span><span class="sxs-lookup"><span data-stu-id="2322c-131">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="2322c-132">id</span><span class="sxs-lookup"><span data-stu-id="2322c-132">id</span></span>|<span data-ttu-id="2322c-133">Cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="2322c-133">String</span></span>|<span data-ttu-id="2322c-134">Chave da entidade.</span><span class="sxs-lookup"><span data-stu-id="2322c-134">Key of the entity.</span></span> <span data-ttu-id="2322c-135">Herdada de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="2322c-135">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="2322c-136">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="2322c-136">lastModifiedDateTime</span></span>|<span data-ttu-id="2322c-137">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="2322c-137">DateTimeOffset</span></span>|<span data-ttu-id="2322c-138">DateTime da última modificação do objeto.</span><span class="sxs-lookup"><span data-stu-id="2322c-138">DateTime the object was last modified.</span></span> <span data-ttu-id="2322c-139">Herdada de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="2322c-139">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="2322c-140">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="2322c-140">roleScopeTagIds</span></span>|<span data-ttu-id="2322c-141">Coleção de cadeias de caracteres</span><span class="sxs-lookup"><span data-stu-id="2322c-141">String collection</span></span>|<span data-ttu-id="2322c-142">Lista de marcas de escopo para esta instância de entidade.</span><span class="sxs-lookup"><span data-stu-id="2322c-142">List of Scope Tags for this Entity instance.</span></span> <span data-ttu-id="2322c-143">Herdada de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="2322c-143">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="2322c-144">supportsScopeTags</span><span class="sxs-lookup"><span data-stu-id="2322c-144">supportsScopeTags</span></span>|<span data-ttu-id="2322c-145">Booliano</span><span class="sxs-lookup"><span data-stu-id="2322c-145">Boolean</span></span>|<span data-ttu-id="2322c-146">Indica se a configuração de dispositivo subjacente é ou não compatível com a atribuição de marcas de escopo.</span><span class="sxs-lookup"><span data-stu-id="2322c-146">Indicates whether or not the underlying Device Configuration supports the assignment of scope tags.</span></span> <span data-ttu-id="2322c-147">A atribuição à propriedade ScopeTags não é permitida quando esse valor é false e as entidades não serão visíveis aos usuários com escopo.</span><span class="sxs-lookup"><span data-stu-id="2322c-147">Assigning to the ScopeTags property is not allowed when this value is false and entities will not be visible to scoped users.</span></span> <span data-ttu-id="2322c-148">Isso ocorre para políticas herdadas criadas no Silverlight e pode ser resolvido excluindo e recriando a política no portal do Azure.</span><span class="sxs-lookup"><span data-stu-id="2322c-148">This occurs for Legacy policies created in Silverlight and can be resolved by deleting and recreating the policy in the Azure Portal.</span></span> <span data-ttu-id="2322c-149">Essa propriedade é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="2322c-149">This property is read-only.</span></span> <span data-ttu-id="2322c-150">Herdada de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="2322c-150">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="2322c-151">deviceManagementApplicabilityRuleOsEdition</span><span class="sxs-lookup"><span data-stu-id="2322c-151">deviceManagementApplicabilityRuleOsEdition</span></span>|[<span data-ttu-id="2322c-152">deviceManagementApplicabilityRuleOsEdition</span><span class="sxs-lookup"><span data-stu-id="2322c-152">deviceManagementApplicabilityRuleOsEdition</span></span>](../resources/intune-deviceconfig-devicemanagementapplicabilityruleosedition.md)|<span data-ttu-id="2322c-153">A aplicabilidade da edição do sistema operacional para essa política.</span><span class="sxs-lookup"><span data-stu-id="2322c-153">The OS edition applicability for this Policy.</span></span> <span data-ttu-id="2322c-154">Herdada de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="2322c-154">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="2322c-155">deviceManagementApplicabilityRuleOsVersion</span><span class="sxs-lookup"><span data-stu-id="2322c-155">deviceManagementApplicabilityRuleOsVersion</span></span>|[<span data-ttu-id="2322c-156">deviceManagementApplicabilityRuleOsVersion</span><span class="sxs-lookup"><span data-stu-id="2322c-156">deviceManagementApplicabilityRuleOsVersion</span></span>](../resources/intune-deviceconfig-devicemanagementapplicabilityruleosversion.md)|<span data-ttu-id="2322c-157">A regra de aplicabilidade da versão do sistema operacional para esta política.</span><span class="sxs-lookup"><span data-stu-id="2322c-157">The OS version applicability rule for this Policy.</span></span> <span data-ttu-id="2322c-158">Herdada de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="2322c-158">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="2322c-159">deviceManagementApplicabilityRuleDeviceMode</span><span class="sxs-lookup"><span data-stu-id="2322c-159">deviceManagementApplicabilityRuleDeviceMode</span></span>|[<span data-ttu-id="2322c-160">deviceManagementApplicabilityRuleDeviceMode</span><span class="sxs-lookup"><span data-stu-id="2322c-160">deviceManagementApplicabilityRuleDeviceMode</span></span>](../resources/intune-deviceconfig-devicemanagementapplicabilityruledevicemode.md)|<span data-ttu-id="2322c-161">A regra de aplicabilidade do modo de dispositivo para essa política.</span><span class="sxs-lookup"><span data-stu-id="2322c-161">The device mode applicability rule for this Policy.</span></span> <span data-ttu-id="2322c-162">Herdada de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="2322c-162">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="2322c-163">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="2322c-163">createdDateTime</span></span>|<span data-ttu-id="2322c-164">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="2322c-164">DateTimeOffset</span></span>|<span data-ttu-id="2322c-165">DateTime em que o objeto foi criado.</span><span class="sxs-lookup"><span data-stu-id="2322c-165">DateTime the object was created.</span></span> <span data-ttu-id="2322c-166">Herdada de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="2322c-166">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="2322c-167">descrição</span><span class="sxs-lookup"><span data-stu-id="2322c-167">description</span></span>|<span data-ttu-id="2322c-168">String</span><span class="sxs-lookup"><span data-stu-id="2322c-168">String</span></span>|<span data-ttu-id="2322c-169">O administrador forneceu a descrição da Configuração do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2322c-169">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="2322c-170">Herdada de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="2322c-170">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="2322c-171">displayName</span><span class="sxs-lookup"><span data-stu-id="2322c-171">displayName</span></span>|<span data-ttu-id="2322c-172">String</span><span class="sxs-lookup"><span data-stu-id="2322c-172">String</span></span>|<span data-ttu-id="2322c-173">O administrador forneceu o nome da Configuração do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2322c-173">Admin provided name of the device configuration.</span></span> <span data-ttu-id="2322c-174">Herdada de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="2322c-174">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="2322c-175">versão</span><span class="sxs-lookup"><span data-stu-id="2322c-175">version</span></span>|<span data-ttu-id="2322c-176">Int32</span><span class="sxs-lookup"><span data-stu-id="2322c-176">Int32</span></span>|<span data-ttu-id="2322c-177">Versão da configuração do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2322c-177">Version of the device configuration.</span></span> <span data-ttu-id="2322c-178">Herdada de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="2322c-178">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="2322c-179">authenticationMethod</span><span class="sxs-lookup"><span data-stu-id="2322c-179">authenticationMethod</span></span>|[<span data-ttu-id="2322c-180">vpnAuthenticationMethod</span><span class="sxs-lookup"><span data-stu-id="2322c-180">vpnAuthenticationMethod</span></span>](../resources/intune-deviceconfig-vpnauthenticationmethod.md)|<span data-ttu-id="2322c-181">Método de autenticação.</span><span class="sxs-lookup"><span data-stu-id="2322c-181">Authentication method.</span></span> <span data-ttu-id="2322c-182">Herdado de [vpnConfiguration](../resources/intune-deviceconfig-vpnconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="2322c-182">Inherited from [vpnConfiguration](../resources/intune-deviceconfig-vpnconfiguration.md).</span></span> <span data-ttu-id="2322c-183">Os valores possíveis são: `certificate`, `usernameAndPassword`, `sharedSecret`, `derivedCredential`.</span><span class="sxs-lookup"><span data-stu-id="2322c-183">Possible values are: `certificate`, `usernameAndPassword`, `sharedSecret`, `derivedCredential`.</span></span>|
|<span data-ttu-id="2322c-184">ConnectionName</span><span class="sxs-lookup"><span data-stu-id="2322c-184">connectionName</span></span>|<span data-ttu-id="2322c-185">String</span><span class="sxs-lookup"><span data-stu-id="2322c-185">String</span></span>|<span data-ttu-id="2322c-186">Nome da conexão exibido para o usuário.</span><span class="sxs-lookup"><span data-stu-id="2322c-186">Connection name displayed to the user.</span></span> <span data-ttu-id="2322c-187">Herdado de [vpnConfiguration](../resources/intune-deviceconfig-vpnconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="2322c-187">Inherited from [vpnConfiguration](../resources/intune-deviceconfig-vpnconfiguration.md)</span></span>|
|<span data-ttu-id="2322c-188">role</span><span class="sxs-lookup"><span data-stu-id="2322c-188">role</span></span>|<span data-ttu-id="2322c-189">String</span><span class="sxs-lookup"><span data-stu-id="2322c-189">String</span></span>|<span data-ttu-id="2322c-190">Função quando o tipo de conexão é definido como pulsar seguro.</span><span class="sxs-lookup"><span data-stu-id="2322c-190">Role when connection type is set to Pulse Secure.</span></span> <span data-ttu-id="2322c-191">Herdado de [vpnConfiguration](../resources/intune-deviceconfig-vpnconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="2322c-191">Inherited from [vpnConfiguration](../resources/intune-deviceconfig-vpnconfiguration.md)</span></span>|
|<span data-ttu-id="2322c-192">esfera</span><span class="sxs-lookup"><span data-stu-id="2322c-192">realm</span></span>|<span data-ttu-id="2322c-193">String</span><span class="sxs-lookup"><span data-stu-id="2322c-193">String</span></span>|<span data-ttu-id="2322c-194">O realm quando o tipo de conexão é definido como pulsar seguro.</span><span class="sxs-lookup"><span data-stu-id="2322c-194">Realm when connection type is set to Pulse Secure.</span></span> <span data-ttu-id="2322c-195">Herdado de [vpnConfiguration](../resources/intune-deviceconfig-vpnconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="2322c-195">Inherited from [vpnConfiguration](../resources/intune-deviceconfig-vpnconfiguration.md)</span></span>|
|<span data-ttu-id="2322c-196">servidores</span><span class="sxs-lookup"><span data-stu-id="2322c-196">servers</span></span>|<span data-ttu-id="2322c-197">coleção [vpnServer](../resources/intune-deviceconfig-vpnserver.md)</span><span class="sxs-lookup"><span data-stu-id="2322c-197">[vpnServer](../resources/intune-deviceconfig-vpnserver.md) collection</span></span>|<span data-ttu-id="2322c-198">Lista de servidores VPN na rede.</span><span class="sxs-lookup"><span data-stu-id="2322c-198">List of VPN Servers on the network.</span></span> <span data-ttu-id="2322c-199">Verifique se os usuários finais podem acessar esses locais de rede.</span><span class="sxs-lookup"><span data-stu-id="2322c-199">Make sure end users can access these network locations.</span></span> <span data-ttu-id="2322c-200">Esta coleção pode conter um máximo de 500 elementos.</span><span class="sxs-lookup"><span data-stu-id="2322c-200">This collection can contain a maximum of 500 elements.</span></span> <span data-ttu-id="2322c-201">Herdado de [vpnConfiguration](../resources/intune-deviceconfig-vpnconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="2322c-201">Inherited from [vpnConfiguration](../resources/intune-deviceconfig-vpnconfiguration.md)</span></span>|
|<span data-ttu-id="2322c-202">Connection</span><span class="sxs-lookup"><span data-stu-id="2322c-202">connectionType</span></span>|[<span data-ttu-id="2322c-203">androidVpnConnectionType</span><span class="sxs-lookup"><span data-stu-id="2322c-203">androidVpnConnectionType</span></span>](../resources/intune-deviceconfig-androidvpnconnectiontype.md)|<span data-ttu-id="2322c-204">Tipo de conexão.</span><span class="sxs-lookup"><span data-stu-id="2322c-204">Connection type.</span></span> <span data-ttu-id="2322c-205">Os possíveis valores são: `ciscoAnyConnect`, `pulseSecure`, `f5EdgeClient`, `dellSonicWallMobileConnect`, `checkPointCapsuleVpn`, `citrix`.</span><span class="sxs-lookup"><span data-stu-id="2322c-205">Possible values are: `ciscoAnyConnect`, `pulseSecure`, `f5EdgeClient`, `dellSonicWallMobileConnect`, `checkPointCapsuleVpn`, `citrix`.</span></span>|



## <a name="response"></a><span data-ttu-id="2322c-206">Resposta</span><span class="sxs-lookup"><span data-stu-id="2322c-206">Response</span></span>
<span data-ttu-id="2322c-207">Se tiver êxito, este método retornará `200 OK` um código de resposta e um objeto [androidDeviceOwnerVpnConfiguration](../resources/intune-deviceconfig-androiddeviceownervpnconfiguration.md) atualizado no corpo da resposta.</span><span class="sxs-lookup"><span data-stu-id="2322c-207">If successful, this method returns a `200 OK` response code and an updated [androidDeviceOwnerVpnConfiguration](../resources/intune-deviceconfig-androiddeviceownervpnconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="2322c-208">Exemplo</span><span class="sxs-lookup"><span data-stu-id="2322c-208">Example</span></span>

### <a name="request"></a><span data-ttu-id="2322c-209">Solicitação</span><span class="sxs-lookup"><span data-stu-id="2322c-209">Request</span></span>
<span data-ttu-id="2322c-210">Este é um exemplo da solicitação.</span><span class="sxs-lookup"><span data-stu-id="2322c-210">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations/{deviceConfigurationId}
Content-type: application/json
Content-length: 1417

{
  "@odata.type": "#microsoft.graph.androidDeviceOwnerVpnConfiguration",
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "supportsScopeTags": true,
  "deviceManagementApplicabilityRuleOsEdition": {
    "@odata.type": "microsoft.graph.deviceManagementApplicabilityRuleOsEdition",
    "osEditionTypes": [
      "windows10EnterpriseN"
    ],
    "name": "Name value",
    "ruleType": "exclude"
  },
  "deviceManagementApplicabilityRuleOsVersion": {
    "@odata.type": "microsoft.graph.deviceManagementApplicabilityRuleOsVersion",
    "minOSVersion": "Min OSVersion value",
    "maxOSVersion": "Max OSVersion value",
    "name": "Name value",
    "ruleType": "exclude"
  },
  "deviceManagementApplicabilityRuleDeviceMode": {
    "@odata.type": "microsoft.graph.deviceManagementApplicabilityRuleDeviceMode",
    "deviceMode": "sModeConfiguration",
    "name": "Name value",
    "ruleType": "exclude"
  },
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "authenticationMethod": "usernameAndPassword",
  "connectionName": "Connection Name value",
  "role": "Role value",
  "realm": "Realm value",
  "servers": [
    {
      "@odata.type": "microsoft.graph.vpnServer",
      "description": "Description value",
      "address": "Address value",
      "isDefaultServer": true
    }
  ],
  "connectionType": "pulseSecure"
}
```

### <a name="response"></a><span data-ttu-id="2322c-211">Resposta</span><span class="sxs-lookup"><span data-stu-id="2322c-211">Response</span></span>
<span data-ttu-id="2322c-p119">Veja a seguir um exemplo da resposta. Observação: o objeto response mostrado aqui pode estar truncado por motivos de concisão. Todas as propriedades serão retornadas de uma chamada real.</span><span class="sxs-lookup"><span data-stu-id="2322c-p119">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1589

{
  "@odata.type": "#microsoft.graph.androidDeviceOwnerVpnConfiguration",
  "id": "972962e3-62e3-9729-e362-2997e3622997",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "supportsScopeTags": true,
  "deviceManagementApplicabilityRuleOsEdition": {
    "@odata.type": "microsoft.graph.deviceManagementApplicabilityRuleOsEdition",
    "osEditionTypes": [
      "windows10EnterpriseN"
    ],
    "name": "Name value",
    "ruleType": "exclude"
  },
  "deviceManagementApplicabilityRuleOsVersion": {
    "@odata.type": "microsoft.graph.deviceManagementApplicabilityRuleOsVersion",
    "minOSVersion": "Min OSVersion value",
    "maxOSVersion": "Max OSVersion value",
    "name": "Name value",
    "ruleType": "exclude"
  },
  "deviceManagementApplicabilityRuleDeviceMode": {
    "@odata.type": "microsoft.graph.deviceManagementApplicabilityRuleDeviceMode",
    "deviceMode": "sModeConfiguration",
    "name": "Name value",
    "ruleType": "exclude"
  },
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "authenticationMethod": "usernameAndPassword",
  "connectionName": "Connection Name value",
  "role": "Role value",
  "realm": "Realm value",
  "servers": [
    {
      "@odata.type": "microsoft.graph.vpnServer",
      "description": "Description value",
      "address": "Address value",
      "isDefaultServer": true
    }
  ],
  "connectionType": "pulseSecure"
}
```





