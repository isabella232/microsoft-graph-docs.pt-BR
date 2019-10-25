---
title: Atualizar macOSPkcsCertificateProfile
description: Atualiza as propriedades de um objeto macOSPkcsCertificateProfile.
author: rolyon
localization_priority: Normal
ms.prod: Intune
doc_type: apiPageType
ms.openlocfilehash: f04562de62a1f25232757c0d7257171c67d36d44
ms.sourcegitcommit: 0dcabe677927c259c2ddcefd0d5e2a2aef065e8b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/16/2019
ms.locfileid: "37533457"
---
# <a name="update-macospkcscertificateprofile"></a><span data-ttu-id="53e10-103">Atualizar macOSPkcsCertificateProfile</span><span class="sxs-lookup"><span data-stu-id="53e10-103">Update macOSPkcsCertificateProfile</span></span>

> <span data-ttu-id="53e10-104">**Importante:** As APIs do Microsoft Graph na versão/beta estão sujeitas a alterações; Não há suporte para o uso de produção.</span><span class="sxs-lookup"><span data-stu-id="53e10-104">**Important:** Microsoft Graph APIs under the /beta version are subject to change; production use is not supported.</span></span>

> <span data-ttu-id="53e10-105">**Observação:** A API do Microsoft Graph para Intune requer uma [licença do Active Intune](https://go.microsoft.com/fwlink/?linkid=839381) para o locatário.</span><span class="sxs-lookup"><span data-stu-id="53e10-105">**Note:** The Microsoft Graph API for Intune requires an [active Intune license](https://go.microsoft.com/fwlink/?linkid=839381) for the tenant.</span></span>

<span data-ttu-id="53e10-106">Atualiza as propriedades de um objeto [macOSPkcsCertificateProfile](../resources/intune-deviceconfig-macospkcscertificateprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="53e10-106">Update the properties of a [macOSPkcsCertificateProfile](../resources/intune-deviceconfig-macospkcscertificateprofile.md) object.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="53e10-107">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="53e10-107">Prerequisites</span></span>
<span data-ttu-id="53e10-p101">Uma das seguintes permissões é obrigatória para chamar esta API. Para saber mais, incluindo como escolher permissões, confira [Permissões](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="53e10-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="53e10-110">Tipo de permissão</span><span class="sxs-lookup"><span data-stu-id="53e10-110">Permission type</span></span>|<span data-ttu-id="53e10-111">Permissões (de privilégios máximos a mínimos)</span><span class="sxs-lookup"><span data-stu-id="53e10-111">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="53e10-112">Delegado (conta corporativa ou de estudante)</span><span class="sxs-lookup"><span data-stu-id="53e10-112">Delegated (work or school account)</span></span>|<span data-ttu-id="53e10-113">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="53e10-113">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="53e10-114">Delegado (conta pessoal da Microsoft)</span><span class="sxs-lookup"><span data-stu-id="53e10-114">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="53e10-115">Sem suporte.</span><span class="sxs-lookup"><span data-stu-id="53e10-115">Not supported.</span></span>|
|<span data-ttu-id="53e10-116">Application</span><span class="sxs-lookup"><span data-stu-id="53e10-116">Application</span></span>|<span data-ttu-id="53e10-117">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="53e10-117">DeviceManagementConfiguration.ReadWrite.All</span></span>|

## <a name="http-request"></a><span data-ttu-id="53e10-118">Solicitação HTTP</span><span class="sxs-lookup"><span data-stu-id="53e10-118">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/groupAssignments/{deviceConfigurationGroupAssignmentId}/deviceConfiguration
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations/{deviceConfigurationId}
```

## <a name="request-headers"></a><span data-ttu-id="53e10-119">Cabeçalhos de solicitação</span><span class="sxs-lookup"><span data-stu-id="53e10-119">Request headers</span></span>
|<span data-ttu-id="53e10-120">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="53e10-120">Header</span></span>|<span data-ttu-id="53e10-121">Valor</span><span class="sxs-lookup"><span data-stu-id="53e10-121">Value</span></span>|
|:---|:---|
|<span data-ttu-id="53e10-122">Autorização</span><span class="sxs-lookup"><span data-stu-id="53e10-122">Authorization</span></span>|<span data-ttu-id="53e10-123">&lt;Token&gt; de portador obrigatório.</span><span class="sxs-lookup"><span data-stu-id="53e10-123">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="53e10-124">Aceitar</span><span class="sxs-lookup"><span data-stu-id="53e10-124">Accept</span></span>|<span data-ttu-id="53e10-125">application/json</span><span class="sxs-lookup"><span data-stu-id="53e10-125">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="53e10-126">Corpo da solicitação</span><span class="sxs-lookup"><span data-stu-id="53e10-126">Request body</span></span>
<span data-ttu-id="53e10-127">No corpo da solicitação, forneça uma representação JSON do objeto [macOSPkcsCertificateProfile](../resources/intune-deviceconfig-macospkcscertificateprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="53e10-127">In the request body, supply a JSON representation for the [macOSPkcsCertificateProfile](../resources/intune-deviceconfig-macospkcscertificateprofile.md) object.</span></span>

<span data-ttu-id="53e10-128">A tabela a seguir mostra as propriedades que são necessárias ao criar [macOSPkcsCertificateProfile](../resources/intune-deviceconfig-macospkcscertificateprofile.md).</span><span class="sxs-lookup"><span data-stu-id="53e10-128">The following table shows the properties that are required when you create the [macOSPkcsCertificateProfile](../resources/intune-deviceconfig-macospkcscertificateprofile.md).</span></span>

|<span data-ttu-id="53e10-129">Propriedade</span><span class="sxs-lookup"><span data-stu-id="53e10-129">Property</span></span>|<span data-ttu-id="53e10-130">Tipo</span><span class="sxs-lookup"><span data-stu-id="53e10-130">Type</span></span>|<span data-ttu-id="53e10-131">Descrição</span><span class="sxs-lookup"><span data-stu-id="53e10-131">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="53e10-132">id</span><span class="sxs-lookup"><span data-stu-id="53e10-132">id</span></span>|<span data-ttu-id="53e10-133">Cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="53e10-133">String</span></span>|<span data-ttu-id="53e10-134">Chave da entidade.</span><span class="sxs-lookup"><span data-stu-id="53e10-134">Key of the entity.</span></span> <span data-ttu-id="53e10-135">Herdada de [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="53e10-135">Inherited from [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="53e10-136">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="53e10-136">lastModifiedDateTime</span></span>|<span data-ttu-id="53e10-137">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="53e10-137">DateTimeOffset</span></span>|<span data-ttu-id="53e10-138">DateTime da última modificação do objeto.</span><span class="sxs-lookup"><span data-stu-id="53e10-138">DateTime the object was last modified.</span></span> <span data-ttu-id="53e10-139">Herdada de [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="53e10-139">Inherited from [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="53e10-140">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="53e10-140">roleScopeTagIds</span></span>|<span data-ttu-id="53e10-141">String collection</span><span class="sxs-lookup"><span data-stu-id="53e10-141">String collection</span></span>|<span data-ttu-id="53e10-142">Lista de marcas de escopo para esta instância de entidade.</span><span class="sxs-lookup"><span data-stu-id="53e10-142">List of Scope Tags for this Entity instance.</span></span> <span data-ttu-id="53e10-143">Herdada de [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="53e10-143">Inherited from [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="53e10-144">supportsScopeTags</span><span class="sxs-lookup"><span data-stu-id="53e10-144">supportsScopeTags</span></span>|<span data-ttu-id="53e10-145">Booliano</span><span class="sxs-lookup"><span data-stu-id="53e10-145">Boolean</span></span>|<span data-ttu-id="53e10-146">Indica se a configuração de dispositivo subjacente é ou não compatível com a atribuição de marcas de escopo.</span><span class="sxs-lookup"><span data-stu-id="53e10-146">Indicates whether or not the underlying Device Configuration supports the assignment of scope tags.</span></span> <span data-ttu-id="53e10-147">A atribuição à propriedade ScopeTags não é permitida quando esse valor é false e as entidades não serão visíveis aos usuários com escopo.</span><span class="sxs-lookup"><span data-stu-id="53e10-147">Assigning to the ScopeTags property is not allowed when this value is false and entities will not be visible to scoped users.</span></span> <span data-ttu-id="53e10-148">Isso ocorre para políticas herdadas criadas no Silverlight e pode ser resolvido excluindo e recriando a política no portal do Azure.</span><span class="sxs-lookup"><span data-stu-id="53e10-148">This occurs for Legacy policies created in Silverlight and can be resolved by deleting and recreating the policy in the Azure Portal.</span></span> <span data-ttu-id="53e10-149">Essa propriedade é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="53e10-149">This property is read-only.</span></span> <span data-ttu-id="53e10-150">Herdada de [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="53e10-150">Inherited from [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="53e10-151">deviceManagementApplicabilityRuleOsEdition</span><span class="sxs-lookup"><span data-stu-id="53e10-151">deviceManagementApplicabilityRuleOsEdition</span></span>|[<span data-ttu-id="53e10-152">deviceManagementApplicabilityRuleOsEdition</span><span class="sxs-lookup"><span data-stu-id="53e10-152">deviceManagementApplicabilityRuleOsEdition</span></span>](../resources/intune-deviceconfig-devicemanagementapplicabilityruleosedition.md)|<span data-ttu-id="53e10-153">A aplicabilidade da edição do sistema operacional para essa política.</span><span class="sxs-lookup"><span data-stu-id="53e10-153">The OS edition applicability for this Policy.</span></span> <span data-ttu-id="53e10-154">Herdada de [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="53e10-154">Inherited from [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="53e10-155">deviceManagementApplicabilityRuleOsVersion</span><span class="sxs-lookup"><span data-stu-id="53e10-155">deviceManagementApplicabilityRuleOsVersion</span></span>|[<span data-ttu-id="53e10-156">deviceManagementApplicabilityRuleOsVersion</span><span class="sxs-lookup"><span data-stu-id="53e10-156">deviceManagementApplicabilityRuleOsVersion</span></span>](../resources/intune-deviceconfig-devicemanagementapplicabilityruleosversion.md)|<span data-ttu-id="53e10-157">A regra de aplicabilidade da versão do sistema operacional para esta política.</span><span class="sxs-lookup"><span data-stu-id="53e10-157">The OS version applicability rule for this Policy.</span></span> <span data-ttu-id="53e10-158">Herdada de [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="53e10-158">Inherited from [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="53e10-159">deviceManagementApplicabilityRuleDeviceMode</span><span class="sxs-lookup"><span data-stu-id="53e10-159">deviceManagementApplicabilityRuleDeviceMode</span></span>|[<span data-ttu-id="53e10-160">deviceManagementApplicabilityRuleDeviceMode</span><span class="sxs-lookup"><span data-stu-id="53e10-160">deviceManagementApplicabilityRuleDeviceMode</span></span>](../resources/intune-deviceconfig-devicemanagementapplicabilityruledevicemode.md)|<span data-ttu-id="53e10-161">A regra de aplicabilidade do modo de dispositivo para essa política.</span><span class="sxs-lookup"><span data-stu-id="53e10-161">The device mode applicability rule for this Policy.</span></span> <span data-ttu-id="53e10-162">Herdada de [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="53e10-162">Inherited from [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="53e10-163">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="53e10-163">createdDateTime</span></span>|<span data-ttu-id="53e10-164">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="53e10-164">DateTimeOffset</span></span>|<span data-ttu-id="53e10-165">DateTime em que o objeto foi criado.</span><span class="sxs-lookup"><span data-stu-id="53e10-165">DateTime the object was created.</span></span> <span data-ttu-id="53e10-166">Herdada de [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="53e10-166">Inherited from [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="53e10-167">description</span><span class="sxs-lookup"><span data-stu-id="53e10-167">description</span></span>|<span data-ttu-id="53e10-168">String</span><span class="sxs-lookup"><span data-stu-id="53e10-168">String</span></span>|<span data-ttu-id="53e10-169">O administrador forneceu a descrição da Configuração do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="53e10-169">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="53e10-170">Herdada de [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="53e10-170">Inherited from [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="53e10-171">displayName</span><span class="sxs-lookup"><span data-stu-id="53e10-171">displayName</span></span>|<span data-ttu-id="53e10-172">String</span><span class="sxs-lookup"><span data-stu-id="53e10-172">String</span></span>|<span data-ttu-id="53e10-173">O administrador forneceu o nome da Configuração do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="53e10-173">Admin provided name of the device configuration.</span></span> <span data-ttu-id="53e10-174">Herdada de [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="53e10-174">Inherited from [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="53e10-175">versão</span><span class="sxs-lookup"><span data-stu-id="53e10-175">version</span></span>|<span data-ttu-id="53e10-176">Int32</span><span class="sxs-lookup"><span data-stu-id="53e10-176">Int32</span></span>|<span data-ttu-id="53e10-177">Versão da configuração do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="53e10-177">Version of the device configuration.</span></span> <span data-ttu-id="53e10-178">Herdada de [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="53e10-178">Inherited from [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="53e10-179">renewalThresholdPercentage</span><span class="sxs-lookup"><span data-stu-id="53e10-179">renewalThresholdPercentage</span></span>|<span data-ttu-id="53e10-180">Int32</span><span class="sxs-lookup"><span data-stu-id="53e10-180">Int32</span></span>|<span data-ttu-id="53e10-181">Porcentagem de limite de renovação de certificado.</span><span class="sxs-lookup"><span data-stu-id="53e10-181">Certificate renewal threshold percentage.</span></span> <span data-ttu-id="53e10-182">Herdado de [macOSCertificateProfileBase](../resources/intune-deviceconfig-macoscertificateprofilebase.md)</span><span class="sxs-lookup"><span data-stu-id="53e10-182">Inherited from [macOSCertificateProfileBase](../resources/intune-deviceconfig-macoscertificateprofilebase.md)</span></span>|
|<span data-ttu-id="53e10-183">subjectNameFormat</span><span class="sxs-lookup"><span data-stu-id="53e10-183">subjectNameFormat</span></span>|[<span data-ttu-id="53e10-184">appleSubjectNameFormat</span><span class="sxs-lookup"><span data-stu-id="53e10-184">appleSubjectNameFormat</span></span>](../resources/intune-deviceconfig-applesubjectnameformat.md)|<span data-ttu-id="53e10-185">Formato do nome de entidade do certificado.</span><span class="sxs-lookup"><span data-stu-id="53e10-185">Certificate Subject Name Format.</span></span> <span data-ttu-id="53e10-186">Herdado de [macOSCertificateProfileBase](../resources/intune-deviceconfig-macoscertificateprofilebase.md).</span><span class="sxs-lookup"><span data-stu-id="53e10-186">Inherited from [macOSCertificateProfileBase](../resources/intune-deviceconfig-macoscertificateprofilebase.md).</span></span> <span data-ttu-id="53e10-187">Os possíveis valores são: `commonName`, `commonNameAsEmail`, `custom`, `commonNameIncludingEmail`, `commonNameAsIMEI`, `commonNameAsSerialNumber`.</span><span class="sxs-lookup"><span data-stu-id="53e10-187">Possible values are: `commonName`, `commonNameAsEmail`, `custom`, `commonNameIncludingEmail`, `commonNameAsIMEI`, `commonNameAsSerialNumber`.</span></span>|
|<span data-ttu-id="53e10-188">subjectAlternativeNameType</span><span class="sxs-lookup"><span data-stu-id="53e10-188">subjectAlternativeNameType</span></span>|[<span data-ttu-id="53e10-189">subjectAlternativeNameType</span><span class="sxs-lookup"><span data-stu-id="53e10-189">subjectAlternativeNameType</span></span>](../resources/intune-deviceconfig-subjectalternativenametype.md)|<span data-ttu-id="53e10-190">Tipo de nome alternativo da entidade do certificado.</span><span class="sxs-lookup"><span data-stu-id="53e10-190">Certificate Subject Alternative Name Type.</span></span> <span data-ttu-id="53e10-191">Herdado de [macOSCertificateProfileBase](../resources/intune-deviceconfig-macoscertificateprofilebase.md).</span><span class="sxs-lookup"><span data-stu-id="53e10-191">Inherited from [macOSCertificateProfileBase](../resources/intune-deviceconfig-macoscertificateprofilebase.md).</span></span> <span data-ttu-id="53e10-192">Os valores possíveis são: `none`, `emailAddress`, `userPrincipalName`, `customAzureADAttribute`, `domainNameService`.</span><span class="sxs-lookup"><span data-stu-id="53e10-192">Possible values are: `none`, `emailAddress`, `userPrincipalName`, `customAzureADAttribute`, `domainNameService`.</span></span>|
|<span data-ttu-id="53e10-193">certificateValidityPeriodValue</span><span class="sxs-lookup"><span data-stu-id="53e10-193">certificateValidityPeriodValue</span></span>|<span data-ttu-id="53e10-194">Int32</span><span class="sxs-lookup"><span data-stu-id="53e10-194">Int32</span></span>|<span data-ttu-id="53e10-195">Valor para o período de validade do certificado.</span><span class="sxs-lookup"><span data-stu-id="53e10-195">Value for the Certificate Validity Period.</span></span> <span data-ttu-id="53e10-196">Herdado de [macOSCertificateProfileBase](../resources/intune-deviceconfig-macoscertificateprofilebase.md)</span><span class="sxs-lookup"><span data-stu-id="53e10-196">Inherited from [macOSCertificateProfileBase](../resources/intune-deviceconfig-macoscertificateprofilebase.md)</span></span>|
|<span data-ttu-id="53e10-197">certificateValidityPeriodScale</span><span class="sxs-lookup"><span data-stu-id="53e10-197">certificateValidityPeriodScale</span></span>|[<span data-ttu-id="53e10-198">certificateValidityPeriodScale</span><span class="sxs-lookup"><span data-stu-id="53e10-198">certificateValidityPeriodScale</span></span>](../resources/intune-deviceconfig-certificatevalidityperiodscale.md)|<span data-ttu-id="53e10-199">Dimensionar o período de validade do certificado.</span><span class="sxs-lookup"><span data-stu-id="53e10-199">Scale for the Certificate Validity Period.</span></span> <span data-ttu-id="53e10-200">Herdado de [macOSCertificateProfileBase](../resources/intune-deviceconfig-macoscertificateprofilebase.md).</span><span class="sxs-lookup"><span data-stu-id="53e10-200">Inherited from [macOSCertificateProfileBase](../resources/intune-deviceconfig-macoscertificateprofilebase.md).</span></span> <span data-ttu-id="53e10-201">Os valores possíveis são: `days`, `months`, `years`.</span><span class="sxs-lookup"><span data-stu-id="53e10-201">Possible values are: `days`, `months`, `years`.</span></span>|
|<span data-ttu-id="53e10-202">certificationAuthority</span><span class="sxs-lookup"><span data-stu-id="53e10-202">certificationAuthority</span></span>|<span data-ttu-id="53e10-203">Cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="53e10-203">String</span></span>|<span data-ttu-id="53e10-204">FQDN da autoridade de certificação PKCS.</span><span class="sxs-lookup"><span data-stu-id="53e10-204">PKCS certification authority FQDN.</span></span>|
|<span data-ttu-id="53e10-205">certificationAuthorityName</span><span class="sxs-lookup"><span data-stu-id="53e10-205">certificationAuthorityName</span></span>|<span data-ttu-id="53e10-206">Cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="53e10-206">String</span></span>|<span data-ttu-id="53e10-207">Nome da autoridade de certificação PKCS.</span><span class="sxs-lookup"><span data-stu-id="53e10-207">PKCS certification authority Name.</span></span>|
|<span data-ttu-id="53e10-208">certificateTemplateName</span><span class="sxs-lookup"><span data-stu-id="53e10-208">certificateTemplateName</span></span>|<span data-ttu-id="53e10-209">Cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="53e10-209">String</span></span>|<span data-ttu-id="53e10-210">Nome do modelo de certificado PKCS.</span><span class="sxs-lookup"><span data-stu-id="53e10-210">PKCS certificate template name.</span></span>|
|<span data-ttu-id="53e10-211">Subjectalternativenameformatstring foi</span><span class="sxs-lookup"><span data-stu-id="53e10-211">subjectAlternativeNameFormatString</span></span>|<span data-ttu-id="53e10-212">Cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="53e10-212">String</span></span>|<span data-ttu-id="53e10-213">Cadeia de caracteres de formato que define o nome alternativo da entidade.</span><span class="sxs-lookup"><span data-stu-id="53e10-213">Format string that defines the subject alternative name.</span></span>|
|<span data-ttu-id="53e10-214">subjectNameFormatString</span><span class="sxs-lookup"><span data-stu-id="53e10-214">subjectNameFormatString</span></span>|<span data-ttu-id="53e10-215">Cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="53e10-215">String</span></span>|<span data-ttu-id="53e10-216">Cadeia de caracteres de formato que define o nome da entidade.</span><span class="sxs-lookup"><span data-stu-id="53e10-216">Format string that defines the subject name.</span></span> <span data-ttu-id="53e10-217">Exemplo: CN = {{EmailAddress}}, E = {{EmailAddress}}, OU = usuários corporativos, O = Contoso Corporation, L = Redmond, ST = WA, C = br</span><span class="sxs-lookup"><span data-stu-id="53e10-217">Example: CN={{EmailAddress}},E={{EmailAddress}},OU=Enterprise Users,O=Contoso Corporation,L=Redmond,ST=WA,C=US</span></span>|
|<span data-ttu-id="53e10-218">certificateStore</span><span class="sxs-lookup"><span data-stu-id="53e10-218">certificateStore</span></span>|[<span data-ttu-id="53e10-219">certificateStore</span><span class="sxs-lookup"><span data-stu-id="53e10-219">certificateStore</span></span>](../resources/intune-deviceconfig-certificatestore.md)|<span data-ttu-id="53e10-220">Certificado de repositório de destino.</span><span class="sxs-lookup"><span data-stu-id="53e10-220">Target store certificate.</span></span> <span data-ttu-id="53e10-221">Os valores possíveis são: `user` e `machine`.</span><span class="sxs-lookup"><span data-stu-id="53e10-221">Possible values are: `user`, `machine`.</span></span>|
|<span data-ttu-id="53e10-222">customSubjectAlternativeNames</span><span class="sxs-lookup"><span data-stu-id="53e10-222">customSubjectAlternativeNames</span></span>|<span data-ttu-id="53e10-223">coleção [customSubjectAlternativeName](../resources/intune-deviceconfig-customsubjectalternativename.md)</span><span class="sxs-lookup"><span data-stu-id="53e10-223">[customSubjectAlternativeName](../resources/intune-deviceconfig-customsubjectalternativename.md) collection</span></span>|<span data-ttu-id="53e10-224">Configurações de nome alternativo de entidade personalizada.</span><span class="sxs-lookup"><span data-stu-id="53e10-224">Custom Subject Alternative Name Settings.</span></span> <span data-ttu-id="53e10-225">Esta coleção pode conter um máximo de 500 elementos.</span><span class="sxs-lookup"><span data-stu-id="53e10-225">This collection can contain a maximum of 500 elements.</span></span>|
|<span data-ttu-id="53e10-226">allowAllAppsAccess</span><span class="sxs-lookup"><span data-stu-id="53e10-226">allowAllAppsAccess</span></span>|<span data-ttu-id="53e10-227">Booliano</span><span class="sxs-lookup"><span data-stu-id="53e10-227">Boolean</span></span>|<span data-ttu-id="53e10-228">Configuração AllowAllAppsAccess</span><span class="sxs-lookup"><span data-stu-id="53e10-228">AllowAllAppsAccess setting</span></span>|



## <a name="response"></a><span data-ttu-id="53e10-229">Resposta</span><span class="sxs-lookup"><span data-stu-id="53e10-229">Response</span></span>
<span data-ttu-id="53e10-230">Se tiver êxito, este método retornará `200 OK` um código de resposta e um objeto [macOSPkcsCertificateProfile](../resources/intune-deviceconfig-macospkcscertificateprofile.md) atualizado no corpo da resposta.</span><span class="sxs-lookup"><span data-stu-id="53e10-230">If successful, this method returns a `200 OK` response code and an updated [macOSPkcsCertificateProfile](../resources/intune-deviceconfig-macospkcscertificateprofile.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="53e10-231">Exemplo</span><span class="sxs-lookup"><span data-stu-id="53e10-231">Example</span></span>

### <a name="request"></a><span data-ttu-id="53e10-232">Solicitação</span><span class="sxs-lookup"><span data-stu-id="53e10-232">Request</span></span>
<span data-ttu-id="53e10-233">Este é um exemplo da solicitação.</span><span class="sxs-lookup"><span data-stu-id="53e10-233">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations/{deviceConfigurationId}
Content-type: application/json
Content-length: 1857

{
  "@odata.type": "#microsoft.graph.macOSPkcsCertificateProfile",
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
  "renewalThresholdPercentage": 10,
  "subjectNameFormat": "commonNameAsEmail",
  "subjectAlternativeNameType": "emailAddress",
  "certificateValidityPeriodValue": 14,
  "certificateValidityPeriodScale": "months",
  "certificationAuthority": "Certification Authority value",
  "certificationAuthorityName": "Certification Authority Name value",
  "certificateTemplateName": "Certificate Template Name value",
  "subjectAlternativeNameFormatString": "Subject Alternative Name Format String value",
  "subjectNameFormatString": "Subject Name Format String value",
  "certificateStore": "machine",
  "customSubjectAlternativeNames": [
    {
      "@odata.type": "microsoft.graph.customSubjectAlternativeName",
      "sanType": "emailAddress",
      "name": "Name value"
    }
  ],
  "allowAllAppsAccess": true
}
```

### <a name="response"></a><span data-ttu-id="53e10-234">Resposta</span><span class="sxs-lookup"><span data-stu-id="53e10-234">Response</span></span>
<span data-ttu-id="53e10-p121">Veja a seguir um exemplo da resposta. Observação: o objeto response mostrado aqui pode estar truncado por motivos de concisão. Todas as propriedades serão retornadas de uma chamada real.</span><span class="sxs-lookup"><span data-stu-id="53e10-p121">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 2029

{
  "@odata.type": "#microsoft.graph.macOSPkcsCertificateProfile",
  "id": "4b489237-9237-4b48-3792-484b3792484b",
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
  "renewalThresholdPercentage": 10,
  "subjectNameFormat": "commonNameAsEmail",
  "subjectAlternativeNameType": "emailAddress",
  "certificateValidityPeriodValue": 14,
  "certificateValidityPeriodScale": "months",
  "certificationAuthority": "Certification Authority value",
  "certificationAuthorityName": "Certification Authority Name value",
  "certificateTemplateName": "Certificate Template Name value",
  "subjectAlternativeNameFormatString": "Subject Alternative Name Format String value",
  "subjectNameFormatString": "Subject Name Format String value",
  "certificateStore": "machine",
  "customSubjectAlternativeNames": [
    {
      "@odata.type": "microsoft.graph.customSubjectAlternativeName",
      "sanType": "emailAddress",
      "name": "Name value"
    }
  ],
  "allowAllAppsAccess": true
}
```





