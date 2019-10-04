---
title: Criar mdmWindowsInformationProtectionPolicy
description: Cria um novo objeto mdmWindowsInformationProtectionPolicy.
author: rolyon
localization_priority: Normal
ms.prod: Intune
doc_type: apiPageType
ms.openlocfilehash: 7a49b446280c5707c5bcbf4d7a54056e106cc12c
ms.sourcegitcommit: 86903a4730bbd825eabb7f0a1b2429723cc8b1e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/26/2019
ms.locfileid: "37199403"
---
# <a name="create-mdmwindowsinformationprotectionpolicy"></a><span data-ttu-id="f9859-103">Criar mdmWindowsInformationProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="f9859-103">Create mdmWindowsInformationProtectionPolicy</span></span>

> <span data-ttu-id="f9859-104">**Importante:** As APIs do Microsoft Graph na versão/beta estão sujeitas a alterações; Não há suporte para o uso de produção.</span><span class="sxs-lookup"><span data-stu-id="f9859-104">**Important:** Microsoft Graph APIs under the /beta version are subject to change; production use is not supported.</span></span>

> <span data-ttu-id="f9859-105">**Observação:** A API do Microsoft Graph para Intune requer uma [licença do Active Intune](https://go.microsoft.com/fwlink/?linkid=839381) para o locatário.</span><span class="sxs-lookup"><span data-stu-id="f9859-105">**Note:** The Microsoft Graph API for Intune requires an [active Intune license](https://go.microsoft.com/fwlink/?linkid=839381) for the tenant.</span></span>

<span data-ttu-id="f9859-106">Cria um novo objeto [mdmWindowsInformationProtectionPolicy](../resources/intune-shared-mdmwindowsinformationprotectionpolicy.md).</span><span class="sxs-lookup"><span data-stu-id="f9859-106">Create a new [mdmWindowsInformationProtectionPolicy](../resources/intune-shared-mdmwindowsinformationprotectionpolicy.md) object.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="f9859-107">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="f9859-107">Prerequisites</span></span>
<span data-ttu-id="f9859-p101">Uma das seguintes permissões é obrigatória para chamar esta API. Para saber mais, incluindo como escolher permissões, confira [Permissões](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="f9859-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="f9859-110">Tipo de permissão</span><span class="sxs-lookup"><span data-stu-id="f9859-110">Permission type</span></span>|<span data-ttu-id="f9859-111">Permissões (de privilégios máximos a mínimos)</span><span class="sxs-lookup"><span data-stu-id="f9859-111">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="f9859-112">Delegado (conta corporativa ou de estudante)</span><span class="sxs-lookup"><span data-stu-id="f9859-112">Delegated (work or school account)</span></span>||
| <span data-ttu-id="f9859-113">&nbsp; &nbsp; **Gerenciamento de aplicativo móvel (GAM)**</span><span class="sxs-lookup"><span data-stu-id="f9859-113">&nbsp; &nbsp; **Mobile app management (MAM)**</span></span> | <span data-ttu-id="f9859-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="f9859-114">DeviceManagementApps.ReadWrite.All</span></span>|
| <span data-ttu-id="f9859-115">&nbsp;&nbsp; **Conjunto de políticas**</span><span class="sxs-lookup"><span data-stu-id="f9859-115">&nbsp; &nbsp; **Policy Set**</span></span> | <span data-ttu-id="f9859-116">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="f9859-116">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="f9859-117">Delegado (conta pessoal da Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f9859-117">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="f9859-118">Sem suporte.</span><span class="sxs-lookup"><span data-stu-id="f9859-118">Not supported.</span></span>|
|<span data-ttu-id="f9859-119">Aplicativo</span><span class="sxs-lookup"><span data-stu-id="f9859-119">Application</span></span>||
| <span data-ttu-id="f9859-120">&nbsp; &nbsp; **Gerenciamento de aplicativo móvel (GAM)**</span><span class="sxs-lookup"><span data-stu-id="f9859-120">&nbsp; &nbsp; **Mobile app management (MAM)**</span></span> | <span data-ttu-id="f9859-121">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="f9859-121">DeviceManagementApps.ReadWrite.All</span></span>|
| <span data-ttu-id="f9859-122">&nbsp;&nbsp; **Conjunto de políticas**</span><span class="sxs-lookup"><span data-stu-id="f9859-122">&nbsp; &nbsp; **Policy Set**</span></span> | <span data-ttu-id="f9859-123">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="f9859-123">DeviceManagementApps.ReadWrite.All</span></span>|

## <a name="http-request"></a><span data-ttu-id="f9859-124">Solicitação HTTP</span><span class="sxs-lookup"><span data-stu-id="f9859-124">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/mdmWindowsInformationProtectionPolicies
```

## <a name="request-headers"></a><span data-ttu-id="f9859-125">Cabeçalhos de solicitação</span><span class="sxs-lookup"><span data-stu-id="f9859-125">Request headers</span></span>
|<span data-ttu-id="f9859-126">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="f9859-126">Header</span></span>|<span data-ttu-id="f9859-127">Valor</span><span class="sxs-lookup"><span data-stu-id="f9859-127">Value</span></span>|
|:---|:---|
|<span data-ttu-id="f9859-128">Autorização</span><span class="sxs-lookup"><span data-stu-id="f9859-128">Authorization</span></span>|<span data-ttu-id="f9859-129">&lt;Token&gt; de portador obrigatório.</span><span class="sxs-lookup"><span data-stu-id="f9859-129">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="f9859-130">Aceitar</span><span class="sxs-lookup"><span data-stu-id="f9859-130">Accept</span></span>|<span data-ttu-id="f9859-131">application/json</span><span class="sxs-lookup"><span data-stu-id="f9859-131">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="f9859-132">Corpo da solicitação</span><span class="sxs-lookup"><span data-stu-id="f9859-132">Request body</span></span>
<span data-ttu-id="f9859-133">No corpo da solicitação, forneça uma representação JSON do objeto mdmWindowsInformationProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="f9859-133">In the request body, supply a JSON representation for the mdmWindowsInformationProtectionPolicy object.</span></span>

<span data-ttu-id="f9859-134">A tabela a seguir mostra as propriedades que são necessárias ao criar mdmWindowsInformationProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="f9859-134">The following table shows the properties that are required when you create the mdmWindowsInformationProtectionPolicy.</span></span>

|<span data-ttu-id="f9859-135">Propriedade</span><span class="sxs-lookup"><span data-stu-id="f9859-135">Property</span></span>|<span data-ttu-id="f9859-136">Tipo</span><span class="sxs-lookup"><span data-stu-id="f9859-136">Type</span></span>|<span data-ttu-id="f9859-137">Descrição</span><span class="sxs-lookup"><span data-stu-id="f9859-137">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="f9859-138">displayName</span><span class="sxs-lookup"><span data-stu-id="f9859-138">displayName</span></span>|<span data-ttu-id="f9859-139">String</span><span class="sxs-lookup"><span data-stu-id="f9859-139">String</span></span>|<span data-ttu-id="f9859-140">Nome para exibição da política.</span><span class="sxs-lookup"><span data-stu-id="f9859-140">Policy display name.</span></span> <span data-ttu-id="f9859-141">Herdado de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)</span><span class="sxs-lookup"><span data-stu-id="f9859-141">Inherited from [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)</span></span>|
|<span data-ttu-id="f9859-142">descrição</span><span class="sxs-lookup"><span data-stu-id="f9859-142">description</span></span>|<span data-ttu-id="f9859-143">String</span><span class="sxs-lookup"><span data-stu-id="f9859-143">String</span></span>|<span data-ttu-id="f9859-144">A descrição da política.</span><span class="sxs-lookup"><span data-stu-id="f9859-144">The policy's description.</span></span> <span data-ttu-id="f9859-145">Herdado de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)</span><span class="sxs-lookup"><span data-stu-id="f9859-145">Inherited from [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)</span></span>|
|<span data-ttu-id="f9859-146">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="f9859-146">createdDateTime</span></span>|<span data-ttu-id="f9859-147">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="f9859-147">DateTimeOffset</span></span>|<span data-ttu-id="f9859-148">A data e a hora da criação da política.</span><span class="sxs-lookup"><span data-stu-id="f9859-148">The date and time the policy was created.</span></span> <span data-ttu-id="f9859-149">Herdado de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)</span><span class="sxs-lookup"><span data-stu-id="f9859-149">Inherited from [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)</span></span>|
|<span data-ttu-id="f9859-150">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="f9859-150">lastModifiedDateTime</span></span>|<span data-ttu-id="f9859-151">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="f9859-151">DateTimeOffset</span></span>|<span data-ttu-id="f9859-152">Última vez em que a política foi modificada.</span><span class="sxs-lookup"><span data-stu-id="f9859-152">Last time the policy was modified.</span></span> <span data-ttu-id="f9859-153">Herdado de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)</span><span class="sxs-lookup"><span data-stu-id="f9859-153">Inherited from [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)</span></span>|
|<span data-ttu-id="f9859-154">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="f9859-154">roleScopeTagIds</span></span>|<span data-ttu-id="f9859-155">Coleção de cadeias de caracteres</span><span class="sxs-lookup"><span data-stu-id="f9859-155">String collection</span></span>|<span data-ttu-id="f9859-156">Lista de marcas de escopo para esta instância de entidade.</span><span class="sxs-lookup"><span data-stu-id="f9859-156">List of Scope Tags for this Entity instance.</span></span> <span data-ttu-id="f9859-157">Herdado de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)</span><span class="sxs-lookup"><span data-stu-id="f9859-157">Inherited from [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)</span></span>|
|<span data-ttu-id="f9859-158">id</span><span class="sxs-lookup"><span data-stu-id="f9859-158">id</span></span>|<span data-ttu-id="f9859-159">Cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="f9859-159">String</span></span>|<span data-ttu-id="f9859-160">Chave da entidade.</span><span class="sxs-lookup"><span data-stu-id="f9859-160">Key of the entity.</span></span> <span data-ttu-id="f9859-161">Herdado de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)</span><span class="sxs-lookup"><span data-stu-id="f9859-161">Inherited from [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)</span></span>|
|<span data-ttu-id="f9859-162">version</span><span class="sxs-lookup"><span data-stu-id="f9859-162">version</span></span>|<span data-ttu-id="f9859-163">String</span><span class="sxs-lookup"><span data-stu-id="f9859-163">String</span></span>|<span data-ttu-id="f9859-164">Versão da entidade.</span><span class="sxs-lookup"><span data-stu-id="f9859-164">Version of the entity.</span></span> <span data-ttu-id="f9859-165">Herdado de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)</span><span class="sxs-lookup"><span data-stu-id="f9859-165">Inherited from [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)</span></span>|
|<span data-ttu-id="f9859-166">enforcementLevel</span><span class="sxs-lookup"><span data-stu-id="f9859-166">enforcementLevel</span></span>|[<span data-ttu-id="f9859-167">windowsInformationProtectionEnforcementLevel</span><span class="sxs-lookup"><span data-stu-id="f9859-167">windowsInformationProtectionEnforcementLevel</span></span>](../resources/intune-mam-windowsinformationprotectionenforcementlevel.md)|<span data-ttu-id="f9859-168">Nível de imposição WIP. Confira a definição de enumeração para valores suportados herdados de [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="f9859-168">WIP enforcement level.See the Enum definition for supported values Inherited from [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md).</span></span> <span data-ttu-id="f9859-169">Os valores possíveis são: `noProtection`, `encryptAndAuditOnly`, `encryptAuditAndPrompt`, `encryptAuditAndBlock`.</span><span class="sxs-lookup"><span data-stu-id="f9859-169">Possible values are: `noProtection`, `encryptAndAuditOnly`, `encryptAuditAndPrompt`, `encryptAuditAndBlock`.</span></span>|
|<span data-ttu-id="f9859-170">enterpriseDomain</span><span class="sxs-lookup"><span data-stu-id="f9859-170">enterpriseDomain</span></span>|<span data-ttu-id="f9859-171">String</span><span class="sxs-lookup"><span data-stu-id="f9859-171">String</span></span>|<span data-ttu-id="f9859-172">Domínio primário da empresa Herdado de [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span><span class="sxs-lookup"><span data-stu-id="f9859-172">Primary enterprise domain Inherited from [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="f9859-173">enterpriseProtectedDomainNames</span><span class="sxs-lookup"><span data-stu-id="f9859-173">enterpriseProtectedDomainNames</span></span>|<span data-ttu-id="f9859-174">Coleção [windowsInformationProtectionResourceCollection](../resources/intune-mam-windowsinformationprotectionresourcecollection.md)</span><span class="sxs-lookup"><span data-stu-id="f9859-174">[windowsInformationProtectionResourceCollection](../resources/intune-mam-windowsinformationprotectionresourcecollection.md) collection</span></span>|<span data-ttu-id="f9859-175">Lista de domínios primários da empresa a serem protegidos Herdado de [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span><span class="sxs-lookup"><span data-stu-id="f9859-175">List of enterprise domains to be protected Inherited from [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="f9859-176">protectionUnderLockConfigRequired</span><span class="sxs-lookup"><span data-stu-id="f9859-176">protectionUnderLockConfigRequired</span></span>|<span data-ttu-id="f9859-177">Booliano</span><span class="sxs-lookup"><span data-stu-id="f9859-177">Boolean</span></span>|<span data-ttu-id="f9859-178">Especifica se a proteção no recurso de bloqueio (também conhecido como criptografar com pin) deve ser configurada Herdado de [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span><span class="sxs-lookup"><span data-stu-id="f9859-178">Specifies whether the protection under lock feature (also known as encrypt under pin) should be configured Inherited from [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="f9859-179">dataRecoveryCertificate</span><span class="sxs-lookup"><span data-stu-id="f9859-179">dataRecoveryCertificate</span></span>|[<span data-ttu-id="f9859-180">windowsInformationProtectionDataRecoveryCertificate</span><span class="sxs-lookup"><span data-stu-id="f9859-180">windowsInformationProtectionDataRecoveryCertificate</span></span>](../resources/intune-mam-windowsinformationprotectiondatarecoverycertificate.md)|<span data-ttu-id="f9859-181">Especifica um certificado de recuperação que pode ser usado para recuperação de dados de arquivos criptografados.</span><span class="sxs-lookup"><span data-stu-id="f9859-181">Specifies a recovery certificate that can be used for data recovery of encrypted files.</span></span> <span data-ttu-id="f9859-182">Isso é o mesmo que o certificado do Agente de recuperação de dados (DRA) para sistema de arquivos com criptografia (EFS) Herdado de [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span><span class="sxs-lookup"><span data-stu-id="f9859-182">This is the same as the data recovery agent(DRA) certificate for encrypting file system(EFS) Inherited from [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="f9859-183">revokeOnUnenrollDisabled</span><span class="sxs-lookup"><span data-stu-id="f9859-183">revokeOnUnenrollDisabled</span></span>|<span data-ttu-id="f9859-184">Booliano</span><span class="sxs-lookup"><span data-stu-id="f9859-184">Boolean</span></span>|<span data-ttu-id="f9859-185">Essa política controla se as teclas WIP serão revogadas quando for cancelado o registro de um dispositivo no serviço de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="f9859-185">This policy controls whether to revoke the WIP keys when a device unenrolls from the management service.</span></span> <span data-ttu-id="f9859-186">Se definido como 1 (não revogar teclas), as teclas não serão revogadas e o usuário continuará a ter acesso a arquivos protegidos após o cancelamento de registro.</span><span class="sxs-lookup"><span data-stu-id="f9859-186">If set to 1 (Don't revoke keys), the keys will not be revoked and the user will continue to have access to protected files after unenrollment.</span></span> <span data-ttu-id="f9859-187">Se as teclas não forem revogadas, não haverá limpeza de arquivos revogados posteriormente.</span><span class="sxs-lookup"><span data-stu-id="f9859-187">If the keys are not revoked, there will be no revoked file cleanup subsequently.</span></span> <span data-ttu-id="f9859-188">Herdado de [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span><span class="sxs-lookup"><span data-stu-id="f9859-188">Inherited from [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="f9859-189">rightsManagementServicesTemplateId</span><span class="sxs-lookup"><span data-stu-id="f9859-189">rightsManagementServicesTemplateId</span></span>|<span data-ttu-id="f9859-190">Guid</span><span class="sxs-lookup"><span data-stu-id="f9859-190">Guid</span></span>|<span data-ttu-id="f9859-191">GUID de TemplateID para uso em criptografia RMS.</span><span class="sxs-lookup"><span data-stu-id="f9859-191">TemplateID GUID to use for RMS encryption.</span></span> <span data-ttu-id="f9859-192">O modelo do RMS permite ao administrador de TI configurar os detalhes sobre quem tem acesso a arquivos protegidos por RMS e por quanto tempo tem esse acesso Herdado de [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span><span class="sxs-lookup"><span data-stu-id="f9859-192">The RMS template allows the IT admin to configure the details about who has access to RMS-protected file and how long they have access Inherited from [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="f9859-193">azureRightsManagementServicesAllowed</span><span class="sxs-lookup"><span data-stu-id="f9859-193">azureRightsManagementServicesAllowed</span></span>|<span data-ttu-id="f9859-194">Booliano</span><span class="sxs-lookup"><span data-stu-id="f9859-194">Boolean</span></span>|<span data-ttu-id="f9859-195">Especifica se a criptografia do Azure RMS para WIP será permitida Herdado de [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span><span class="sxs-lookup"><span data-stu-id="f9859-195">Specifies whether to allow Azure RMS encryption for WIP Inherited from [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="f9859-196">iconsVisible</span><span class="sxs-lookup"><span data-stu-id="f9859-196">iconsVisible</span></span>|<span data-ttu-id="f9859-197">Booliano</span><span class="sxs-lookup"><span data-stu-id="f9859-197">Boolean</span></span>|<span data-ttu-id="f9859-198">Determina se sobreposições são adicionadas a ícones em arquivos protegido por WIP no Explorador e em blocos de aplicativos somente para empresas no menu Iniciar.</span><span class="sxs-lookup"><span data-stu-id="f9859-198">Determines whether overlays are added to icons for WIP protected files in Explorer and enterprise only app tiles in the Start menu.</span></span> <span data-ttu-id="f9859-199">A partir do Windows 10, versão 1703, essa configuração também define a visibilidade do ícone WIP na barra de título de um aplicativo protegido por WIP Herdado de [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span><span class="sxs-lookup"><span data-stu-id="f9859-199">Starting in Windows 10, version 1703 this setting also configures the visibility of the WIP icon in the title bar of a WIP-protected app Inherited from [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="f9859-200">protectedApps</span><span class="sxs-lookup"><span data-stu-id="f9859-200">protectedApps</span></span>|<span data-ttu-id="f9859-201">Coleção [windowsInformationProtectionApp](../resources/intune-mam-windowsinformationprotectionapp.md)</span><span class="sxs-lookup"><span data-stu-id="f9859-201">[windowsInformationProtectionApp](../resources/intune-mam-windowsinformationprotectionapp.md) collection</span></span>|<span data-ttu-id="f9859-202">Os aplicativos protegidos podem acessar dados corporativos e os dados manipulados por esses aplicativos são protegidos com criptografia Herdado de [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span><span class="sxs-lookup"><span data-stu-id="f9859-202">Protected applications can access enterprise data and the data handled by those applications are protected with encryption Inherited from [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="f9859-203">exemptApps</span><span class="sxs-lookup"><span data-stu-id="f9859-203">exemptApps</span></span>|<span data-ttu-id="f9859-204">Coleção [windowsInformationProtectionApp](../resources/intune-mam-windowsinformationprotectionapp.md)</span><span class="sxs-lookup"><span data-stu-id="f9859-204">[windowsInformationProtectionApp](../resources/intune-mam-windowsinformationprotectionapp.md) collection</span></span>|<span data-ttu-id="f9859-205">Os aplicativos isentos também podem acessar dados corporativos, mas os dados manipulados por esses aplicativos não são protegidos.</span><span class="sxs-lookup"><span data-stu-id="f9859-205">Exempt applications can also access enterprise data, but the data handled by those applications are not protected.</span></span> <span data-ttu-id="f9859-206">Isso ocorre porque alguns aplicativos corporativos essenciais podem ter problemas de compatibilidade com dados criptografados.</span><span class="sxs-lookup"><span data-stu-id="f9859-206">This is because some critical enterprise applications may have compatibility problems with encrypted data.</span></span> <span data-ttu-id="f9859-207">Herdado de [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span><span class="sxs-lookup"><span data-stu-id="f9859-207">Inherited from [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="f9859-208">enterpriseNetworkDomainNames</span><span class="sxs-lookup"><span data-stu-id="f9859-208">enterpriseNetworkDomainNames</span></span>|<span data-ttu-id="f9859-209">Coleção [windowsInformationProtectionResourceCollection](../resources/intune-mam-windowsinformationprotectionresourcecollection.md)</span><span class="sxs-lookup"><span data-stu-id="f9859-209">[windowsInformationProtectionResourceCollection](../resources/intune-mam-windowsinformationprotectionresourcecollection.md) collection</span></span>|<span data-ttu-id="f9859-210">Esta é a lista dos domínios que compõem os limites da empresa.</span><span class="sxs-lookup"><span data-stu-id="f9859-210">This is the list of domains that comprise the boundaries of the enterprise.</span></span> <span data-ttu-id="f9859-211">Os dados de um desses domínios enviados para um dispositivo serão considerados dados corporativos e serão protegidos Esses locais serão considerados um destino seguro para que dados corporativos sejam compartilhados Herdado de [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span><span class="sxs-lookup"><span data-stu-id="f9859-211">Data from one of these domains that is sent to a device will be considered enterprise data and protected These locations will be considered a safe destination for enterprise data to be shared to Inherited from [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="f9859-212">enterpriseProxiedDomains</span><span class="sxs-lookup"><span data-stu-id="f9859-212">enterpriseProxiedDomains</span></span>|<span data-ttu-id="f9859-213">Coleção [windowsInformationProtectionProxiedDomainCollection](../resources/intune-mam-windowsinformationprotectionproxieddomaincollection.md)</span><span class="sxs-lookup"><span data-stu-id="f9859-213">[windowsInformationProtectionProxiedDomainCollection](../resources/intune-mam-windowsinformationprotectionproxieddomaincollection.md) collection</span></span>|<span data-ttu-id="f9859-214">Contém uma lista de domínios de recursos da empresa hospedado na nuvem que precisam ser protegidos.</span><span class="sxs-lookup"><span data-stu-id="f9859-214">Contains a list of Enterprise resource domains hosted in the cloud that need to be protected.</span></span> <span data-ttu-id="f9859-215">As conexões com esses recursos são consideradas dados corporativos.</span><span class="sxs-lookup"><span data-stu-id="f9859-215">Connections to these resources are considered enterprise data.</span></span> <span data-ttu-id="f9859-216">Se um proxy for emparelhado com um recurso de nuvem, o tráfego para esse recurso será roteado pela rede da empresa por meio do servidor proxy indicado (na porta 80).</span><span class="sxs-lookup"><span data-stu-id="f9859-216">If a proxy is paired with a cloud resource, traffic to the cloud resource will be routed through the enterprise network via the denoted proxy server (on Port 80).</span></span> <span data-ttu-id="f9859-217">Um servidor proxy usado com essa finalidade também deve ser configurado usando a política EnterpriseInternalProxyServers Herdado de [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span><span class="sxs-lookup"><span data-stu-id="f9859-217">A proxy server used for this purpose must also be configured using the EnterpriseInternalProxyServers policy Inherited from [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="f9859-218">enterpriseIPRanges</span><span class="sxs-lookup"><span data-stu-id="f9859-218">enterpriseIPRanges</span></span>|<span data-ttu-id="f9859-219">Coleção [windowsInformationProtectionIPRangeCollection](../resources/intune-mam-windowsinformationprotectioniprangecollection.md)</span><span class="sxs-lookup"><span data-stu-id="f9859-219">[windowsInformationProtectionIPRangeCollection](../resources/intune-mam-windowsinformationprotectioniprangecollection.md) collection</span></span>|<span data-ttu-id="f9859-220">Define os intervalos IP da empresa que definem os computadores da rede corporativa.</span><span class="sxs-lookup"><span data-stu-id="f9859-220">Sets the enterprise IP ranges that define the computers in the enterprise network.</span></span> <span data-ttu-id="f9859-221">Dados provenientes desses computadores serão considerados parte da empresa e serão protegidos.</span><span class="sxs-lookup"><span data-stu-id="f9859-221">Data that comes from those computers will be considered part of the enterprise and protected.</span></span> <span data-ttu-id="f9859-222">Esses locais serão considerados um destino seguro para que dados corporativos sejam compartilhados Herdado de [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span><span class="sxs-lookup"><span data-stu-id="f9859-222">These locations will be considered a safe destination for enterprise data to be shared to Inherited from [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="f9859-223">enterpriseIPRangesAreAuthoritative</span><span class="sxs-lookup"><span data-stu-id="f9859-223">enterpriseIPRangesAreAuthoritative</span></span>|<span data-ttu-id="f9859-224">Boolean</span><span class="sxs-lookup"><span data-stu-id="f9859-224">Boolean</span></span>|<span data-ttu-id="f9859-225">Valor booliano que informa ao cliente para aceitar a lista configurada e não usar heurística para tentar localizar outras sub-redes.</span><span class="sxs-lookup"><span data-stu-id="f9859-225">Boolean value that tells the client to accept the configured list and not to use heuristics to attempt to find other subnets.</span></span> <span data-ttu-id="f9859-226">A padrão é false Herdado de [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span><span class="sxs-lookup"><span data-stu-id="f9859-226">Default is false Inherited from [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="f9859-227">enterpriseProxyServers</span><span class="sxs-lookup"><span data-stu-id="f9859-227">enterpriseProxyServers</span></span>|<span data-ttu-id="f9859-228">Coleção [windowsInformationProtectionResourceCollection](../resources/intune-mam-windowsinformationprotectionresourcecollection.md)</span><span class="sxs-lookup"><span data-stu-id="f9859-228">[windowsInformationProtectionResourceCollection](../resources/intune-mam-windowsinformationprotectionresourcecollection.md) collection</span></span>|<span data-ttu-id="f9859-229">Esta é uma lista de servidores proxy.</span><span class="sxs-lookup"><span data-stu-id="f9859-229">This is a list of proxy servers.</span></span> <span data-ttu-id="f9859-230">Qualquer servidor que não esteja na lista é considerado não corporativo Herdado de [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span><span class="sxs-lookup"><span data-stu-id="f9859-230">Any server not on this list is considered non-enterprise Inherited from [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="f9859-231">enterpriseInternalProxyServers</span><span class="sxs-lookup"><span data-stu-id="f9859-231">enterpriseInternalProxyServers</span></span>|<span data-ttu-id="f9859-232">Coleção [windowsInformationProtectionResourceCollection](../resources/intune-mam-windowsinformationprotectionresourcecollection.md)</span><span class="sxs-lookup"><span data-stu-id="f9859-232">[windowsInformationProtectionResourceCollection](../resources/intune-mam-windowsinformationprotectionresourcecollection.md) collection</span></span>|<span data-ttu-id="f9859-233">Esta é a lista separada por vírgula de servidores proxy internos.</span><span class="sxs-lookup"><span data-stu-id="f9859-233">This is the comma-separated list of internal proxy servers.</span></span> <span data-ttu-id="f9859-234">Por exemplo, "157.54.14.28, 157.54.11.118, 10.202.14.167, 157.53.14.163, 157.69.210.59".</span><span class="sxs-lookup"><span data-stu-id="f9859-234">For example, "157.54.14.28, 157.54.11.118, 10.202.14.167, 157.53.14.163, 157.69.210.59".</span></span> <span data-ttu-id="f9859-235">Esses proxies foram configurados pelo administrador para se conectarem a recursos específicos na Internet.</span><span class="sxs-lookup"><span data-stu-id="f9859-235">These proxies have been configured by the admin to connect to specific resources on the Internet.</span></span> <span data-ttu-id="f9859-236">Eles são considerados locais de rede da empresa.</span><span class="sxs-lookup"><span data-stu-id="f9859-236">They are considered to be enterprise network locations.</span></span> <span data-ttu-id="f9859-237">Os proxies são utilizados somente na configuração da política EnterpriseProxiedDomains para forçar o tráfego para os domínios correspondentes por meio desses proxies Herdado de [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span><span class="sxs-lookup"><span data-stu-id="f9859-237">The proxies are only leveraged in configuring the EnterpriseProxiedDomains policy to force traffic to the matched domains through these proxies Inherited from [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="f9859-238">enterpriseProxyServersAreAuthoritative</span><span class="sxs-lookup"><span data-stu-id="f9859-238">enterpriseProxyServersAreAuthoritative</span></span>|<span data-ttu-id="f9859-239">Booliano</span><span class="sxs-lookup"><span data-stu-id="f9859-239">Boolean</span></span>|<span data-ttu-id="f9859-240">Valor booliano que informa ao cliente para aceitar a lista configurada de proxies e não tentar detectar outros proxies de trabalho.</span><span class="sxs-lookup"><span data-stu-id="f9859-240">Boolean value that tells the client to accept the configured list of proxies and not try to detect other work proxies.</span></span> <span data-ttu-id="f9859-241">A padrão é false Herdado de [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span><span class="sxs-lookup"><span data-stu-id="f9859-241">Default is false Inherited from [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="f9859-242">neutralDomainResources</span><span class="sxs-lookup"><span data-stu-id="f9859-242">neutralDomainResources</span></span>|<span data-ttu-id="f9859-243">Coleção [windowsInformationProtectionResourceCollection](../resources/intune-mam-windowsinformationprotectionresourcecollection.md)</span><span class="sxs-lookup"><span data-stu-id="f9859-243">[windowsInformationProtectionResourceCollection](../resources/intune-mam-windowsinformationprotectionresourcecollection.md) collection</span></span>|<span data-ttu-id="f9859-244">Lista de nomes de domínio que podem ser usados para recurso de trabalho ou pessoal Herdado de [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span><span class="sxs-lookup"><span data-stu-id="f9859-244">List of domain names that can used for work or personal resource Inherited from [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="f9859-245">indexingEncryptedStoresOrItemsBlocked</span><span class="sxs-lookup"><span data-stu-id="f9859-245">indexingEncryptedStoresOrItemsBlocked</span></span>|<span data-ttu-id="f9859-246">Boolean</span><span class="sxs-lookup"><span data-stu-id="f9859-246">Boolean</span></span>|<span data-ttu-id="f9859-247">Esta opção é para o indexador do Windows Search para permitir ou não a indexação de itens Herdado do [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span><span class="sxs-lookup"><span data-stu-id="f9859-247">This switch is for the Windows Search Indexer, to allow or disallow indexing of items Inherited from [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="f9859-248">smbAutoEncryptedFileExtensions</span><span class="sxs-lookup"><span data-stu-id="f9859-248">smbAutoEncryptedFileExtensions</span></span>|<span data-ttu-id="f9859-249">Coleção [windowsInformationProtectionResourceCollection](../resources/intune-mam-windowsinformationprotectionresourcecollection.md)</span><span class="sxs-lookup"><span data-stu-id="f9859-249">[windowsInformationProtectionResourceCollection](../resources/intune-mam-windowsinformationprotectionresourcecollection.md) collection</span></span>|<span data-ttu-id="f9859-250">Especifica uma lista de extensões de arquivo para que os arquivos com essas extensões sejam criptografados quando copiados de um compartilhamento SMB dentro do limite corporativo Herdado de [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span><span class="sxs-lookup"><span data-stu-id="f9859-250">Specifies a list of file extensions, so that files with these extensions are encrypted when copying from an SMB share within the corporate boundary Inherited from [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="f9859-251">isAssigned</span><span class="sxs-lookup"><span data-stu-id="f9859-251">isAssigned</span></span>|<span data-ttu-id="f9859-252">Booliano</span><span class="sxs-lookup"><span data-stu-id="f9859-252">Boolean</span></span>|<span data-ttu-id="f9859-253">Indica se a política foi implantada a grupos de inclusão ou não.</span><span class="sxs-lookup"><span data-stu-id="f9859-253">Indicates if the policy is deployed to any inclusion groups or not.</span></span> <span data-ttu-id="f9859-254">Herdado de [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span><span class="sxs-lookup"><span data-stu-id="f9859-254">Inherited from [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span></span>|



## <a name="response"></a><span data-ttu-id="f9859-255">Resposta</span><span class="sxs-lookup"><span data-stu-id="f9859-255">Response</span></span>
<span data-ttu-id="f9859-256">Se bem-sucedido, este método retornará um código de resposta `201 Created` e um objeto [mdmWindowsInformationProtectionPolicy](../resources/intune-shared-mdmwindowsinformationprotectionpolicy.md) no corpo da resposta.</span><span class="sxs-lookup"><span data-stu-id="f9859-256">If successful, this method returns a `201 Created` response code and a [mdmWindowsInformationProtectionPolicy](../resources/intune-shared-mdmwindowsinformationprotectionpolicy.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="f9859-257">Exemplo</span><span class="sxs-lookup"><span data-stu-id="f9859-257">Example</span></span>

### <a name="request"></a><span data-ttu-id="f9859-258">Solicitação</span><span class="sxs-lookup"><span data-stu-id="f9859-258">Request</span></span>
<span data-ttu-id="f9859-259">Este é um exemplo da solicitação.</span><span class="sxs-lookup"><span data-stu-id="f9859-259">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceAppManagement/mdmWindowsInformationProtectionPolicies
Content-type: application/json
Content-length: 3967

{
  "@odata.type": "#microsoft.graph.mdmWindowsInformationProtectionPolicy",
  "displayName": "Display Name value",
  "description": "Description value",
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "version": "Version value",
  "enforcementLevel": "encryptAndAuditOnly",
  "enterpriseDomain": "Enterprise Domain value",
  "enterpriseProtectedDomainNames": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionResourceCollection",
      "displayName": "Display Name value",
      "resources": [
        "Resources value"
      ]
    }
  ],
  "protectionUnderLockConfigRequired": true,
  "dataRecoveryCertificate": {
    "@odata.type": "microsoft.graph.windowsInformationProtectionDataRecoveryCertificate",
    "subjectName": "Subject Name value",
    "description": "Description value",
    "expirationDateTime": "2016-12-31T23:57:57.2481234-08:00",
    "certificate": "Y2VydGlmaWNhdGU="
  },
  "revokeOnUnenrollDisabled": true,
  "rightsManagementServicesTemplateId": "abf7b16f-b16f-abf7-6fb1-f7ab6fb1f7ab",
  "azureRightsManagementServicesAllowed": true,
  "iconsVisible": true,
  "protectedApps": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionStoreApp",
      "displayName": "Display Name value",
      "description": "Description value",
      "publisherName": "Publisher Name value",
      "productName": "Product Name value",
      "denied": true
    }
  ],
  "exemptApps": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionStoreApp",
      "displayName": "Display Name value",
      "description": "Description value",
      "publisherName": "Publisher Name value",
      "productName": "Product Name value",
      "denied": true
    }
  ],
  "enterpriseNetworkDomainNames": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionResourceCollection",
      "displayName": "Display Name value",
      "resources": [
        "Resources value"
      ]
    }
  ],
  "enterpriseProxiedDomains": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionProxiedDomainCollection",
      "displayName": "Display Name value",
      "proxiedDomains": [
        {
          "@odata.type": "microsoft.graph.proxiedDomain",
          "ipAddressOrFQDN": "Ip Address Or FQDN value",
          "proxy": "Proxy value"
        }
      ]
    }
  ],
  "enterpriseIPRanges": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionIPRangeCollection",
      "displayName": "Display Name value",
      "ranges": [
        {
          "@odata.type": "microsoft.graph.iPv6Range",
          "lowerAddress": "Lower Address value",
          "upperAddress": "Upper Address value"
        }
      ]
    }
  ],
  "enterpriseIPRangesAreAuthoritative": true,
  "enterpriseProxyServers": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionResourceCollection",
      "displayName": "Display Name value",
      "resources": [
        "Resources value"
      ]
    }
  ],
  "enterpriseInternalProxyServers": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionResourceCollection",
      "displayName": "Display Name value",
      "resources": [
        "Resources value"
      ]
    }
  ],
  "enterpriseProxyServersAreAuthoritative": true,
  "neutralDomainResources": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionResourceCollection",
      "displayName": "Display Name value",
      "resources": [
        "Resources value"
      ]
    }
  ],
  "indexingEncryptedStoresOrItemsBlocked": true,
  "smbAutoEncryptedFileExtensions": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionResourceCollection",
      "displayName": "Display Name value",
      "resources": [
        "Resources value"
      ]
    }
  ],
  "isAssigned": true
}
```

### <a name="response"></a><span data-ttu-id="f9859-260">Resposta</span><span class="sxs-lookup"><span data-stu-id="f9859-260">Response</span></span>
<span data-ttu-id="f9859-p123">Veja a seguir um exemplo da resposta. Observação: o objeto response mostrado aqui pode estar truncado por motivos de concisão. Todas as propriedades serão retornadas de uma chamada real.</span><span class="sxs-lookup"><span data-stu-id="f9859-p123">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 4139

{
  "@odata.type": "#microsoft.graph.mdmWindowsInformationProtectionPolicy",
  "displayName": "Display Name value",
  "description": "Description value",
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "id": "8efb0c35-0c35-8efb-350c-fb8e350cfb8e",
  "version": "Version value",
  "enforcementLevel": "encryptAndAuditOnly",
  "enterpriseDomain": "Enterprise Domain value",
  "enterpriseProtectedDomainNames": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionResourceCollection",
      "displayName": "Display Name value",
      "resources": [
        "Resources value"
      ]
    }
  ],
  "protectionUnderLockConfigRequired": true,
  "dataRecoveryCertificate": {
    "@odata.type": "microsoft.graph.windowsInformationProtectionDataRecoveryCertificate",
    "subjectName": "Subject Name value",
    "description": "Description value",
    "expirationDateTime": "2016-12-31T23:57:57.2481234-08:00",
    "certificate": "Y2VydGlmaWNhdGU="
  },
  "revokeOnUnenrollDisabled": true,
  "rightsManagementServicesTemplateId": "abf7b16f-b16f-abf7-6fb1-f7ab6fb1f7ab",
  "azureRightsManagementServicesAllowed": true,
  "iconsVisible": true,
  "protectedApps": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionStoreApp",
      "displayName": "Display Name value",
      "description": "Description value",
      "publisherName": "Publisher Name value",
      "productName": "Product Name value",
      "denied": true
    }
  ],
  "exemptApps": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionStoreApp",
      "displayName": "Display Name value",
      "description": "Description value",
      "publisherName": "Publisher Name value",
      "productName": "Product Name value",
      "denied": true
    }
  ],
  "enterpriseNetworkDomainNames": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionResourceCollection",
      "displayName": "Display Name value",
      "resources": [
        "Resources value"
      ]
    }
  ],
  "enterpriseProxiedDomains": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionProxiedDomainCollection",
      "displayName": "Display Name value",
      "proxiedDomains": [
        {
          "@odata.type": "microsoft.graph.proxiedDomain",
          "ipAddressOrFQDN": "Ip Address Or FQDN value",
          "proxy": "Proxy value"
        }
      ]
    }
  ],
  "enterpriseIPRanges": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionIPRangeCollection",
      "displayName": "Display Name value",
      "ranges": [
        {
          "@odata.type": "microsoft.graph.iPv6Range",
          "lowerAddress": "Lower Address value",
          "upperAddress": "Upper Address value"
        }
      ]
    }
  ],
  "enterpriseIPRangesAreAuthoritative": true,
  "enterpriseProxyServers": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionResourceCollection",
      "displayName": "Display Name value",
      "resources": [
        "Resources value"
      ]
    }
  ],
  "enterpriseInternalProxyServers": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionResourceCollection",
      "displayName": "Display Name value",
      "resources": [
        "Resources value"
      ]
    }
  ],
  "enterpriseProxyServersAreAuthoritative": true,
  "neutralDomainResources": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionResourceCollection",
      "displayName": "Display Name value",
      "resources": [
        "Resources value"
      ]
    }
  ],
  "indexingEncryptedStoresOrItemsBlocked": true,
  "smbAutoEncryptedFileExtensions": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionResourceCollection",
      "displayName": "Display Name value",
      "resources": [
        "Resources value"
      ]
    }
  ],
  "isAssigned": true
}
```



