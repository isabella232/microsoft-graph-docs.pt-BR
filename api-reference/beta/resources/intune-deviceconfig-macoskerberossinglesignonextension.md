---
title: tipo de recurso macOSKerberosSingleSignOnExtension
description: Representa um perfil de extensão de logon único de tipo Kerberos para dispositivos MacOS.
author: rolyon
localization_priority: Normal
ms.prod: Intune
doc_type: resourcePageType
ms.openlocfilehash: 0e3ffa045508c878d95ee0b7e274de69b64297aa
ms.sourcegitcommit: 86903a4730bbd825eabb7f0a1b2429723cc8b1e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/26/2019
ms.locfileid: "37199681"
---
# <a name="macoskerberossinglesignonextension-resource-type"></a><span data-ttu-id="ddc82-103">tipo de recurso macOSKerberosSingleSignOnExtension</span><span class="sxs-lookup"><span data-stu-id="ddc82-103">macOSKerberosSingleSignOnExtension resource type</span></span>

> <span data-ttu-id="ddc82-104">**Importante:** As APIs do Microsoft Graph na versão/beta estão sujeitas a alterações; Não há suporte para o uso de produção.</span><span class="sxs-lookup"><span data-stu-id="ddc82-104">**Important:** Microsoft Graph APIs under the /beta version are subject to change; production use is not supported.</span></span>

> <span data-ttu-id="ddc82-105">**Observação:** A API do Microsoft Graph para Intune requer uma [licença do Active Intune](https://go.microsoft.com/fwlink/?linkid=839381) para o locatário.</span><span class="sxs-lookup"><span data-stu-id="ddc82-105">**Note:** The Microsoft Graph API for Intune requires an [active Intune license](https://go.microsoft.com/fwlink/?linkid=839381) for the tenant.</span></span>

<span data-ttu-id="ddc82-106">Representa um perfil de extensão de logon único de tipo Kerberos para dispositivos MacOS.</span><span class="sxs-lookup"><span data-stu-id="ddc82-106">Represents a Kerberos-type Single Sign-On extension profile for MacOS devices.</span></span>


<span data-ttu-id="ddc82-107">Herda de [kerberosSingleSignOnExtension](../resources/intune-deviceconfig-kerberossinglesignonextension.md)</span><span class="sxs-lookup"><span data-stu-id="ddc82-107">Inherits from [kerberosSingleSignOnExtension](../resources/intune-deviceconfig-kerberossinglesignonextension.md)</span></span>

## <a name="properties"></a><span data-ttu-id="ddc82-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ddc82-108">Properties</span></span>
|<span data-ttu-id="ddc82-109">Propriedade</span><span class="sxs-lookup"><span data-stu-id="ddc82-109">Property</span></span>|<span data-ttu-id="ddc82-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="ddc82-110">Type</span></span>|<span data-ttu-id="ddc82-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="ddc82-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="ddc82-112">esfera</span><span class="sxs-lookup"><span data-stu-id="ddc82-112">realm</span></span>|<span data-ttu-id="ddc82-113">String</span><span class="sxs-lookup"><span data-stu-id="ddc82-113">String</span></span>|<span data-ttu-id="ddc82-114">Obtém ou define o nome de território que diferencia maiúsculas de minúsculas para esse perfil.</span><span class="sxs-lookup"><span data-stu-id="ddc82-114">Gets or sets the case-sensitive realm name for this profile.</span></span> <span data-ttu-id="ddc82-115">Herdado de [kerberosSingleSignOnExtension](../resources/intune-deviceconfig-kerberossinglesignonextension.md)</span><span class="sxs-lookup"><span data-stu-id="ddc82-115">Inherited from [kerberosSingleSignOnExtension](../resources/intune-deviceconfig-kerberossinglesignonextension.md)</span></span>|
|<span data-ttu-id="ddc82-116">domínio</span><span class="sxs-lookup"><span data-stu-id="ddc82-116">domains</span></span>|<span data-ttu-id="ddc82-117">Coleção de cadeias de caracteres</span><span class="sxs-lookup"><span data-stu-id="ddc82-117">String collection</span></span>|<span data-ttu-id="ddc82-118">Obtém ou define uma lista de hosts ou nomes de domínio para os quais a extensão de aplicativo executa SSO.</span><span class="sxs-lookup"><span data-stu-id="ddc82-118">Gets or sets a list of hosts or domain names for which the app extension performs SSO.</span></span> <span data-ttu-id="ddc82-119">Herdado de [kerberosSingleSignOnExtension](../resources/intune-deviceconfig-kerberossinglesignonextension.md)</span><span class="sxs-lookup"><span data-stu-id="ddc82-119">Inherited from [kerberosSingleSignOnExtension](../resources/intune-deviceconfig-kerberossinglesignonextension.md)</span></span>|
|<span data-ttu-id="ddc82-120">blockAutomaticLogin</span><span class="sxs-lookup"><span data-stu-id="ddc82-120">blockAutomaticLogin</span></span>|<span data-ttu-id="ddc82-121">Booliano</span><span class="sxs-lookup"><span data-stu-id="ddc82-121">Boolean</span></span>|<span data-ttu-id="ddc82-122">Habilita ou desabilita o uso do chaveiro.</span><span class="sxs-lookup"><span data-stu-id="ddc82-122">Enables or disables Keychain usage.</span></span> <span data-ttu-id="ddc82-123">Herdado de [kerberosSingleSignOnExtension](../resources/intune-deviceconfig-kerberossinglesignonextension.md)</span><span class="sxs-lookup"><span data-stu-id="ddc82-123">Inherited from [kerberosSingleSignOnExtension](../resources/intune-deviceconfig-kerberossinglesignonextension.md)</span></span>|
|<span data-ttu-id="ddc82-124">CacheName</span><span class="sxs-lookup"><span data-stu-id="ddc82-124">cacheName</span></span>|<span data-ttu-id="ddc82-125">String</span><span class="sxs-lookup"><span data-stu-id="ddc82-125">String</span></span>|<span data-ttu-id="ddc82-126">Obtém ou define o nome genérico dos serviços de segurança do cache Kerberos a ser usado para esse perfil.</span><span class="sxs-lookup"><span data-stu-id="ddc82-126">Gets or sets the Generic Security Services name of the Kerberos cache to use for this profile.</span></span> <span data-ttu-id="ddc82-127">Herdado de [kerberosSingleSignOnExtension](../resources/intune-deviceconfig-kerberossinglesignonextension.md)</span><span class="sxs-lookup"><span data-stu-id="ddc82-127">Inherited from [kerberosSingleSignOnExtension](../resources/intune-deviceconfig-kerberossinglesignonextension.md)</span></span>|
|<span data-ttu-id="ddc82-128">credentialBundleIdAccessControlList</span><span class="sxs-lookup"><span data-stu-id="ddc82-128">credentialBundleIdAccessControlList</span></span>|<span data-ttu-id="ddc82-129">Coleção de cadeias de caracteres</span><span class="sxs-lookup"><span data-stu-id="ddc82-129">String collection</span></span>|<span data-ttu-id="ddc82-130">Obtém ou define uma lista de IDs de lote de aplicativos que têm permissão para acessar o tíquete de concessão de tíquete Kerberos.</span><span class="sxs-lookup"><span data-stu-id="ddc82-130">Gets or sets a list of app Bundle IDs allowed to access the Kerberos Ticket Granting Ticket.</span></span> <span data-ttu-id="ddc82-131">Herdado de [kerberosSingleSignOnExtension](../resources/intune-deviceconfig-kerberossinglesignonextension.md)</span><span class="sxs-lookup"><span data-stu-id="ddc82-131">Inherited from [kerberosSingleSignOnExtension](../resources/intune-deviceconfig-kerberossinglesignonextension.md)</span></span>|
|<span data-ttu-id="ddc82-132">domainRealms</span><span class="sxs-lookup"><span data-stu-id="ddc82-132">domainRealms</span></span>|<span data-ttu-id="ddc82-133">Coleção de cadeias de caracteres</span><span class="sxs-lookup"><span data-stu-id="ddc82-133">String collection</span></span>|<span data-ttu-id="ddc82-134">Obtém ou define uma lista de Realms para o mapeamento do realm do domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="ddc82-134">Gets or sets a list of realms for custom domain-realm mapping.</span></span> <span data-ttu-id="ddc82-135">Os territórios diferenciam maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="ddc82-135">Realms are case sensitive.</span></span> <span data-ttu-id="ddc82-136">Herdado de [kerberosSingleSignOnExtension](../resources/intune-deviceconfig-kerberossinglesignonextension.md)</span><span class="sxs-lookup"><span data-stu-id="ddc82-136">Inherited from [kerberosSingleSignOnExtension](../resources/intune-deviceconfig-kerberossinglesignonextension.md)</span></span>|
|<span data-ttu-id="ddc82-137">isDefaultRealm</span><span class="sxs-lookup"><span data-stu-id="ddc82-137">isDefaultRealm</span></span>|<span data-ttu-id="ddc82-138">Booliano</span><span class="sxs-lookup"><span data-stu-id="ddc82-138">Boolean</span></span>|<span data-ttu-id="ddc82-139">Quando for true, o realm deste perfil será selecionado como o padrão.</span><span class="sxs-lookup"><span data-stu-id="ddc82-139">When true, this profile's realm will be selected as the default.</span></span> <span data-ttu-id="ddc82-140">Necessário se vários perfis de tipo Kerberos estiverem configurados.</span><span class="sxs-lookup"><span data-stu-id="ddc82-140">Necessary if multiple Kerberos-type profiles are configured.</span></span> <span data-ttu-id="ddc82-141">Herdado de [kerberosSingleSignOnExtension](../resources/intune-deviceconfig-kerberossinglesignonextension.md)</span><span class="sxs-lookup"><span data-stu-id="ddc82-141">Inherited from [kerberosSingleSignOnExtension](../resources/intune-deviceconfig-kerberossinglesignonextension.md)</span></span>|
|<span data-ttu-id="ddc82-142">passwordBlockModification</span><span class="sxs-lookup"><span data-stu-id="ddc82-142">passwordBlockModification</span></span>|<span data-ttu-id="ddc82-143">Booliano</span><span class="sxs-lookup"><span data-stu-id="ddc82-143">Boolean</span></span>|<span data-ttu-id="ddc82-144">Habilita ou desabilita as alterações de senha.</span><span class="sxs-lookup"><span data-stu-id="ddc82-144">Enables or disables password changes.</span></span> <span data-ttu-id="ddc82-145">Herdado de [kerberosSingleSignOnExtension](../resources/intune-deviceconfig-kerberossinglesignonextension.md)</span><span class="sxs-lookup"><span data-stu-id="ddc82-145">Inherited from [kerberosSingleSignOnExtension](../resources/intune-deviceconfig-kerberossinglesignonextension.md)</span></span>|
|<span data-ttu-id="ddc82-146">passwordExpirationDays</span><span class="sxs-lookup"><span data-stu-id="ddc82-146">passwordExpirationDays</span></span>|<span data-ttu-id="ddc82-147">Int32</span><span class="sxs-lookup"><span data-stu-id="ddc82-147">Int32</span></span>|<span data-ttu-id="ddc82-148">Substitui a expiração padrão da senha em dias.</span><span class="sxs-lookup"><span data-stu-id="ddc82-148">Overrides the default password expiration in days.</span></span> <span data-ttu-id="ddc82-149">Para a maioria dos domínios, esse valor é calculado automaticamente.</span><span class="sxs-lookup"><span data-stu-id="ddc82-149">For most domains, this value is calculated automatically.</span></span> <span data-ttu-id="ddc82-150">Herdado de [kerberosSingleSignOnExtension](../resources/intune-deviceconfig-kerberossinglesignonextension.md)</span><span class="sxs-lookup"><span data-stu-id="ddc82-150">Inherited from [kerberosSingleSignOnExtension](../resources/intune-deviceconfig-kerberossinglesignonextension.md)</span></span>|
|<span data-ttu-id="ddc82-151">passwordExpirationNotificationDays</span><span class="sxs-lookup"><span data-stu-id="ddc82-151">passwordExpirationNotificationDays</span></span>|<span data-ttu-id="ddc82-152">Int32</span><span class="sxs-lookup"><span data-stu-id="ddc82-152">Int32</span></span>|<span data-ttu-id="ddc82-153">Obtém ou define o número de dias até que o usuário seja notificado de que sua senha irá expirar (o padrão é 15).</span><span class="sxs-lookup"><span data-stu-id="ddc82-153">Gets or sets the number of days until the user is notified that their password will expire (default is 15).</span></span> <span data-ttu-id="ddc82-154">Herdado de [kerberosSingleSignOnExtension](../resources/intune-deviceconfig-kerberossinglesignonextension.md)</span><span class="sxs-lookup"><span data-stu-id="ddc82-154">Inherited from [kerberosSingleSignOnExtension](../resources/intune-deviceconfig-kerberossinglesignonextension.md)</span></span>|
|<span data-ttu-id="ddc82-155">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="ddc82-155">userPrincipalName</span></span>|<span data-ttu-id="ddc82-156">String</span><span class="sxs-lookup"><span data-stu-id="ddc82-156">String</span></span>|<span data-ttu-id="ddc82-157">Obtém ou define o nome de usuário de princípio a ser usado para esse perfil.</span><span class="sxs-lookup"><span data-stu-id="ddc82-157">Gets or sets the principle user name to use for this profile.</span></span> <span data-ttu-id="ddc82-158">O nome do Realm não precisa ser incluído.</span><span class="sxs-lookup"><span data-stu-id="ddc82-158">The realm name does not need to be included.</span></span> <span data-ttu-id="ddc82-159">Herdado de [kerberosSingleSignOnExtension](../resources/intune-deviceconfig-kerberossinglesignonextension.md)</span><span class="sxs-lookup"><span data-stu-id="ddc82-159">Inherited from [kerberosSingleSignOnExtension](../resources/intune-deviceconfig-kerberossinglesignonextension.md)</span></span>|
|<span data-ttu-id="ddc82-160">passwordRequireActiveDirectoryComplexity</span><span class="sxs-lookup"><span data-stu-id="ddc82-160">passwordRequireActiveDirectoryComplexity</span></span>|<span data-ttu-id="ddc82-161">Booliano</span><span class="sxs-lookup"><span data-stu-id="ddc82-161">Boolean</span></span>|<span data-ttu-id="ddc82-162">Habilita ou desabilita se as senhas devem atender aos requisitos de complexidade do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="ddc82-162">Enables or disables whether passwords must meet Active Directory's complexity requirements.</span></span> <span data-ttu-id="ddc82-163">Herdado de [kerberosSingleSignOnExtension](../resources/intune-deviceconfig-kerberossinglesignonextension.md)</span><span class="sxs-lookup"><span data-stu-id="ddc82-163">Inherited from [kerberosSingleSignOnExtension](../resources/intune-deviceconfig-kerberossinglesignonextension.md)</span></span>|
|<span data-ttu-id="ddc82-164">passwordPreviousPasswordBlockCount</span><span class="sxs-lookup"><span data-stu-id="ddc82-164">passwordPreviousPasswordBlockCount</span></span>|<span data-ttu-id="ddc82-165">Int32</span><span class="sxs-lookup"><span data-stu-id="ddc82-165">Int32</span></span>|<span data-ttu-id="ddc82-166">Obtém ou define o número de senhas anteriores para bloquear.</span><span class="sxs-lookup"><span data-stu-id="ddc82-166">Gets or sets the number of previous passwords to block.</span></span> <span data-ttu-id="ddc82-167">Herdado de [kerberosSingleSignOnExtension](../resources/intune-deviceconfig-kerberossinglesignonextension.md)</span><span class="sxs-lookup"><span data-stu-id="ddc82-167">Inherited from [kerberosSingleSignOnExtension](../resources/intune-deviceconfig-kerberossinglesignonextension.md)</span></span>|
|<span data-ttu-id="ddc82-168">passwordMinimumLength</span><span class="sxs-lookup"><span data-stu-id="ddc82-168">passwordMinimumLength</span></span>|<span data-ttu-id="ddc82-169">Int32</span><span class="sxs-lookup"><span data-stu-id="ddc82-169">Int32</span></span>|<span data-ttu-id="ddc82-170">Obtém ou define o comprimento mínimo de uma senha.</span><span class="sxs-lookup"><span data-stu-id="ddc82-170">Gets or sets the minimum length of a password.</span></span> <span data-ttu-id="ddc82-171">Herdado de [kerberosSingleSignOnExtension](../resources/intune-deviceconfig-kerberossinglesignonextension.md)</span><span class="sxs-lookup"><span data-stu-id="ddc82-171">Inherited from [kerberosSingleSignOnExtension](../resources/intune-deviceconfig-kerberossinglesignonextension.md)</span></span>|
|<span data-ttu-id="ddc82-172">passwordMinimumAgeDays</span><span class="sxs-lookup"><span data-stu-id="ddc82-172">passwordMinimumAgeDays</span></span>|<span data-ttu-id="ddc82-173">Int32</span><span class="sxs-lookup"><span data-stu-id="ddc82-173">Int32</span></span>|<span data-ttu-id="ddc82-174">Obtém ou define o número mínimo de dias até que um usuário possa alterar sua senha novamente.</span><span class="sxs-lookup"><span data-stu-id="ddc82-174">Gets or sets the minimum number of days until a user can change their password again.</span></span> <span data-ttu-id="ddc82-175">Herdado de [kerberosSingleSignOnExtension](../resources/intune-deviceconfig-kerberossinglesignonextension.md)</span><span class="sxs-lookup"><span data-stu-id="ddc82-175">Inherited from [kerberosSingleSignOnExtension](../resources/intune-deviceconfig-kerberossinglesignonextension.md)</span></span>|
|<span data-ttu-id="ddc82-176">passwordRequirementsDescription</span><span class="sxs-lookup"><span data-stu-id="ddc82-176">passwordRequirementsDescription</span></span>|<span data-ttu-id="ddc82-177">String</span><span class="sxs-lookup"><span data-stu-id="ddc82-177">String</span></span>|<span data-ttu-id="ddc82-178">Obtém ou define uma descrição dos requisitos de complexidade de senha.</span><span class="sxs-lookup"><span data-stu-id="ddc82-178">Gets or sets a description of the password complexity requirements.</span></span> <span data-ttu-id="ddc82-179">Herdado de [kerberosSingleSignOnExtension](../resources/intune-deviceconfig-kerberossinglesignonextension.md)</span><span class="sxs-lookup"><span data-stu-id="ddc82-179">Inherited from [kerberosSingleSignOnExtension](../resources/intune-deviceconfig-kerberossinglesignonextension.md)</span></span>|
|<span data-ttu-id="ddc82-180">requireUserPresence</span><span class="sxs-lookup"><span data-stu-id="ddc82-180">requireUserPresence</span></span>|<span data-ttu-id="ddc82-181">Booliano</span><span class="sxs-lookup"><span data-stu-id="ddc82-181">Boolean</span></span>|<span data-ttu-id="ddc82-182">Obtém ou define se deve exigir autenticação por meio de ID de toque, ID de face ou uma senha para acessar a entrada de keychain.</span><span class="sxs-lookup"><span data-stu-id="ddc82-182">Gets or sets whether to require authentication via Touch ID, Face ID, or a passcode to access the keychain entry.</span></span> <span data-ttu-id="ddc82-183">Herdado de [kerberosSingleSignOnExtension](../resources/intune-deviceconfig-kerberossinglesignonextension.md)</span><span class="sxs-lookup"><span data-stu-id="ddc82-183">Inherited from [kerberosSingleSignOnExtension](../resources/intune-deviceconfig-kerberossinglesignonextension.md)</span></span>|
|<span data-ttu-id="ddc82-184">activeDirectorySiteCode</span><span class="sxs-lookup"><span data-stu-id="ddc82-184">activeDirectorySiteCode</span></span>|<span data-ttu-id="ddc82-185">String</span><span class="sxs-lookup"><span data-stu-id="ddc82-185">String</span></span>|<span data-ttu-id="ddc82-186">Obtém ou define o site do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="ddc82-186">Gets or sets the Active Directory site.</span></span> <span data-ttu-id="ddc82-187">Herdado de [kerberosSingleSignOnExtension](../resources/intune-deviceconfig-kerberossinglesignonextension.md)</span><span class="sxs-lookup"><span data-stu-id="ddc82-187">Inherited from [kerberosSingleSignOnExtension](../resources/intune-deviceconfig-kerberossinglesignonextension.md)</span></span>|
|<span data-ttu-id="ddc82-188">passwordEnableLocalSync</span><span class="sxs-lookup"><span data-stu-id="ddc82-188">passwordEnableLocalSync</span></span>|<span data-ttu-id="ddc82-189">Booliano</span><span class="sxs-lookup"><span data-stu-id="ddc82-189">Boolean</span></span>|<span data-ttu-id="ddc82-190">Habilita ou desabilita a sincronização de senha.</span><span class="sxs-lookup"><span data-stu-id="ddc82-190">Enables or disables password syncing.</span></span> <span data-ttu-id="ddc82-191">Isso não afetará os usuários conectados com uma conta móvel no macOS.</span><span class="sxs-lookup"><span data-stu-id="ddc82-191">This won't affect users logged in with a mobile account on macOS.</span></span> <span data-ttu-id="ddc82-192">Herdado de [kerberosSingleSignOnExtension](../resources/intune-deviceconfig-kerberossinglesignonextension.md)</span><span class="sxs-lookup"><span data-stu-id="ddc82-192">Inherited from [kerberosSingleSignOnExtension](../resources/intune-deviceconfig-kerberossinglesignonextension.md)</span></span>|
|<span data-ttu-id="ddc82-193">blockActiveDirectorySiteAutoDiscovery</span><span class="sxs-lookup"><span data-stu-id="ddc82-193">blockActiveDirectorySiteAutoDiscovery</span></span>|<span data-ttu-id="ddc82-194">Booliano</span><span class="sxs-lookup"><span data-stu-id="ddc82-194">Boolean</span></span>|<span data-ttu-id="ddc82-195">Habilita ou desabilita se a extensão Kerberos pode determinar automaticamente o nome do site.</span><span class="sxs-lookup"><span data-stu-id="ddc82-195">Enables or disables whether the Kerberos extension can automatically determine its site name.</span></span> <span data-ttu-id="ddc82-196">Herdado de [kerberosSingleSignOnExtension](../resources/intune-deviceconfig-kerberossinglesignonextension.md)</span><span class="sxs-lookup"><span data-stu-id="ddc82-196">Inherited from [kerberosSingleSignOnExtension](../resources/intune-deviceconfig-kerberossinglesignonextension.md)</span></span>|

## <a name="relationships"></a><span data-ttu-id="ddc82-197">Relações</span><span class="sxs-lookup"><span data-stu-id="ddc82-197">Relationships</span></span>
<span data-ttu-id="ddc82-198">Nenhum</span><span class="sxs-lookup"><span data-stu-id="ddc82-198">None</span></span>

## <a name="json-representation"></a><span data-ttu-id="ddc82-199">Representação JSON</span><span class="sxs-lookup"><span data-stu-id="ddc82-199">JSON Representation</span></span>
<span data-ttu-id="ddc82-200">Veja a seguir uma representação JSON do recurso.</span><span class="sxs-lookup"><span data-stu-id="ddc82-200">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.macOSKerberosSingleSignOnExtension"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.macOSKerberosSingleSignOnExtension",
  "realm": "String",
  "domains": [
    "String"
  ],
  "blockAutomaticLogin": true,
  "cacheName": "String",
  "credentialBundleIdAccessControlList": [
    "String"
  ],
  "domainRealms": [
    "String"
  ],
  "isDefaultRealm": true,
  "passwordBlockModification": true,
  "passwordExpirationDays": 1024,
  "passwordExpirationNotificationDays": 1024,
  "userPrincipalName": "String",
  "passwordRequireActiveDirectoryComplexity": true,
  "passwordPreviousPasswordBlockCount": 1024,
  "passwordMinimumLength": 1024,
  "passwordMinimumAgeDays": 1024,
  "passwordRequirementsDescription": "String",
  "requireUserPresence": true,
  "activeDirectorySiteCode": "String",
  "passwordEnableLocalSync": true,
  "blockActiveDirectorySiteAutoDiscovery": true
}
```


