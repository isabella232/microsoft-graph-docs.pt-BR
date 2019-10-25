---
title: tipo de recurso orgContact
description: Representa um contato organizacional
localization_priority: Normal
author: davidmu1
ms.prod: microsoft-identity-platform
doc_type: resourcePageType
ms.openlocfilehash: a6c604fa008c66447457f1c5736a31df0f39f28b
ms.sourcegitcommit: c9b9ff2c862f8d96d282a7bdf641cdb9c53a4600
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/22/2019
ms.locfileid: "37622581"
---
# <a name="orgcontact-resource-type"></a><span data-ttu-id="edf28-103">tipo de recurso orgContact</span><span class="sxs-lookup"><span data-stu-id="edf28-103">orgContact resource type</span></span>

<span data-ttu-id="edf28-104">Representa um contato organizacional.</span><span class="sxs-lookup"><span data-stu-id="edf28-104">Represents an organizational contact.</span></span> <span data-ttu-id="edf28-105">Os contatos organizacionais são gerenciados pelos administradores de uma organização e são diferentes dos [contatos pessoais](contact.md).</span><span class="sxs-lookup"><span data-stu-id="edf28-105">Organizational contacts are managed by an organization's administrators and are different from [personal contacts](contact.md).</span></span> <span data-ttu-id="edf28-106">Além disso, os contatos organizacionais são sincronizados a partir dos diretórios locais ou do Exchange Online e são somente leitura.</span><span class="sxs-lookup"><span data-stu-id="edf28-106">Additionally, organizational contacts are either synchronized from on-premises directories or from Exchange Online, and are read-only.</span></span>

<span data-ttu-id="edf28-107">Herda do [directoryObject](directoryobject.md).</span><span class="sxs-lookup"><span data-stu-id="edf28-107">Inherits from [directoryObject](directoryobject.md).</span></span>

## <a name="methods"></a><span data-ttu-id="edf28-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="edf28-108">Methods</span></span>

| <span data-ttu-id="edf28-109">Método</span><span class="sxs-lookup"><span data-stu-id="edf28-109">Method</span></span>           | <span data-ttu-id="edf28-110">Tipo de retorno</span><span class="sxs-lookup"><span data-stu-id="edf28-110">Return Type</span></span>    |<span data-ttu-id="edf28-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="edf28-111">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="edf28-112">Listar contatos da organização</span><span class="sxs-lookup"><span data-stu-id="edf28-112">List organizationl contacts</span></span>](../api/orgcontact-list.md) | [<span data-ttu-id="edf28-113">orgContact</span><span class="sxs-lookup"><span data-stu-id="edf28-113">orgContact</span></span>](orgcontact.md) |<span data-ttu-id="edf28-114">Listar Propriedades de contatos organizacionais.</span><span class="sxs-lookup"><span data-stu-id="edf28-114">List properties of organizational contacts.</span></span>|
|[<span data-ttu-id="edf28-115">Obter contato da organização</span><span class="sxs-lookup"><span data-stu-id="edf28-115">Get organizationl contact</span></span>](../api/orgcontact-get.md) | [<span data-ttu-id="edf28-116">orgContact</span><span class="sxs-lookup"><span data-stu-id="edf28-116">orgContact</span></span>](orgcontact.md) |<span data-ttu-id="edf28-117">Leia as propriedades e as relações de um contato organizacional.</span><span class="sxs-lookup"><span data-stu-id="edf28-117">Read properties and relationships of an organizational contact.</span></span>|
|[<span data-ttu-id="edf28-118">Obter gerente</span><span class="sxs-lookup"><span data-stu-id="edf28-118">Get manager</span></span>](../api/orgcontact-get-manager.md) |[<span data-ttu-id="edf28-119">directoryObject</span><span class="sxs-lookup"><span data-stu-id="edf28-119">directoryObject</span></span>](directoryobject.md)| <span data-ttu-id="edf28-120">Obtenha o gerente do contato organizacional.</span><span class="sxs-lookup"><span data-stu-id="edf28-120">Get the organizational contact's manager.</span></span>|
|[<span data-ttu-id="edf28-121">Listar directReports</span><span class="sxs-lookup"><span data-stu-id="edf28-121">List directReports</span></span>](../api/orgcontact-list-directreports.md) |<span data-ttu-id="edf28-122">Coleção [directoryObject](directoryobject.md)</span><span class="sxs-lookup"><span data-stu-id="edf28-122">[directoryObject](directoryobject.md) collection</span></span>| <span data-ttu-id="edf28-123">Listar os subordinados diretos do contato organizacional.</span><span class="sxs-lookup"><span data-stu-id="edf28-123">List the organizational contact's direct reports.</span></span>|
|[<span data-ttu-id="edf28-124">Listar memberOf</span><span class="sxs-lookup"><span data-stu-id="edf28-124">List memberOf</span></span>](../api/orgcontact-list-memberof.md) |<span data-ttu-id="edf28-125">[directoryObject](directoryobject.md) collection</span><span class="sxs-lookup"><span data-stu-id="edf28-125">[directoryObject](directoryobject.md) collection</span></span>| <span data-ttu-id="edf28-126">Listar os grupos dos quais um contato organizacional é membro.</span><span class="sxs-lookup"><span data-stu-id="edf28-126">List the groups an organizational contact is a member of.</span></span>|
|[<span data-ttu-id="edf28-127">Listar transitiveMemberOf</span><span class="sxs-lookup"><span data-stu-id="edf28-127">List transitiveMemberOf</span></span>](../api/orgcontact-list-transitivememberof.md) |<span data-ttu-id="edf28-128">Coleção [directoryObject](directoryobject.md)</span><span class="sxs-lookup"><span data-stu-id="edf28-128">[directoryObject](directoryobject.md) collection</span></span>| <span data-ttu-id="edf28-129">Listar os grupos dos quais um contato organizacional é membro, incluindo grupos nos quais o contato organizacional está aninhado.</span><span class="sxs-lookup"><span data-stu-id="edf28-129">List the groups an organizational contact is a member of, including groups that the organizational contact is nested under.</span></span>|
|[<span data-ttu-id="edf28-130">checkMemberGroups</span><span class="sxs-lookup"><span data-stu-id="edf28-130">checkMemberGroups</span></span>](../api/orgcontact-checkmembergroups.md)|<span data-ttu-id="edf28-131">Coleção de cadeias de caracteres</span><span class="sxs-lookup"><span data-stu-id="edf28-131">String collection</span></span>| <span data-ttu-id="edf28-132">Verifique a associação ao grupo.</span><span class="sxs-lookup"><span data-stu-id="edf28-132">Check for group membership.</span></span> |
|[<span data-ttu-id="edf28-133">getMemberGroups</span><span class="sxs-lookup"><span data-stu-id="edf28-133">getMemberGroups</span></span>](../api/orgcontact-getmembergroups.md)|<span data-ttu-id="edf28-134">String collection</span><span class="sxs-lookup"><span data-stu-id="edf28-134">String collection</span></span>| <span data-ttu-id="edf28-135">Retornar todos os grupos dos quais o contato organizacional especificado é membro.</span><span class="sxs-lookup"><span data-stu-id="edf28-135">Return all the groups that the specified organizational contact is a member of.</span></span> |
|[<span data-ttu-id="edf28-136">getMemberObjects</span><span class="sxs-lookup"><span data-stu-id="edf28-136">getMemberObjects</span></span>](../api/orgcontact-getmemberobjects.md)|<span data-ttu-id="edf28-137">String collection</span><span class="sxs-lookup"><span data-stu-id="edf28-137">String collection</span></span>| <span data-ttu-id="edf28-138">Retorna uma lista de directoryObjects o contato organizacional é um membro.</span><span class="sxs-lookup"><span data-stu-id="edf28-138">Returns a list of directoryObjects the organizational contact is a member of.</span></span> |

## <a name="properties"></a><span data-ttu-id="edf28-139">Propriedades</span><span class="sxs-lookup"><span data-stu-id="edf28-139">Properties</span></span>

| <span data-ttu-id="edf28-140">Propriedade</span><span class="sxs-lookup"><span data-stu-id="edf28-140">Property</span></span>     | <span data-ttu-id="edf28-141">Tipo</span><span class="sxs-lookup"><span data-stu-id="edf28-141">Type</span></span>   |<span data-ttu-id="edf28-142">Descrição</span><span class="sxs-lookup"><span data-stu-id="edf28-142">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="edf28-143">endereços</span><span class="sxs-lookup"><span data-stu-id="edf28-143">addresses</span></span>                    | <span data-ttu-id="edf28-144">coleção [physicalOfficeAddress](physicalofficeaddress.md)</span><span class="sxs-lookup"><span data-stu-id="edf28-144">[physicalOfficeAddress](physicalofficeaddress.md) collection</span></span>           | <span data-ttu-id="edf28-145">Endereços postais para este contato organizacional.</span><span class="sxs-lookup"><span data-stu-id="edf28-145">Postal addresses for this organizational contact.</span></span> <span data-ttu-id="edf28-146">Por enquanto, um contato só pode ter um endereço físico.</span><span class="sxs-lookup"><span data-stu-id="edf28-146">For now a contact can only have one physical address.</span></span> |
| <span data-ttu-id="edf28-147">companyName</span><span class="sxs-lookup"><span data-stu-id="edf28-147">companyName</span></span>                  | <span data-ttu-id="edf28-148">String</span><span class="sxs-lookup"><span data-stu-id="edf28-148">String</span></span>                                                    | <span data-ttu-id="edf28-149">Nome da empresa à qual este contato organizacional pertence.</span><span class="sxs-lookup"><span data-stu-id="edf28-149">Name of the company that this organizational contact belong to.</span></span>                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="edf28-150">department</span><span class="sxs-lookup"><span data-stu-id="edf28-150">department</span></span>                   | <span data-ttu-id="edf28-151">String</span><span class="sxs-lookup"><span data-stu-id="edf28-151">String</span></span>                                                     | <span data-ttu-id="edf28-152">O nome do departamento no qual o contato funciona.</span><span class="sxs-lookup"><span data-stu-id="edf28-152">The name for the department in which the contact works.</span></span>                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="edf28-153">displayName</span><span class="sxs-lookup"><span data-stu-id="edf28-153">displayName</span></span>                  | <span data-ttu-id="edf28-154">Cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="edf28-154">String</span></span>                                                     | <span data-ttu-id="edf28-155">Nome para exibição desse contato organizacional.</span><span class="sxs-lookup"><span data-stu-id="edf28-155">Display name for this organizational contact.</span></span>                                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="edf28-156">givenName</span><span class="sxs-lookup"><span data-stu-id="edf28-156">givenName</span></span>                    | <span data-ttu-id="edf28-157">String</span><span class="sxs-lookup"><span data-stu-id="edf28-157">String</span></span>                                                     | <span data-ttu-id="edf28-158">Nome para este contato organizacional.</span><span class="sxs-lookup"><span data-stu-id="edf28-158">First name for this organizational contact.</span></span>                                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="edf28-159">id</span><span class="sxs-lookup"><span data-stu-id="edf28-159">id</span></span>                           | <span data-ttu-id="edf28-160">String</span><span class="sxs-lookup"><span data-stu-id="edf28-160">String</span></span>                                                     | <span data-ttu-id="edf28-161">Identificador exclusivo desse contato organizacional.</span><span class="sxs-lookup"><span data-stu-id="edf28-161">Unique identifier for this organizational contact.</span></span>                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="edf28-162">jobTitle</span><span class="sxs-lookup"><span data-stu-id="edf28-162">jobTitle</span></span>                     | <span data-ttu-id="edf28-163">String</span><span class="sxs-lookup"><span data-stu-id="edf28-163">String</span></span>                                                     | <span data-ttu-id="edf28-164">Cargo para este contato organizacional.</span><span class="sxs-lookup"><span data-stu-id="edf28-164">Job title for this organizational contact.</span></span>                                                                                                                                                                                                                                                                                                                                      |
|<span data-ttu-id="edf28-165">email</span><span class="sxs-lookup"><span data-stu-id="edf28-165">mail</span></span>|<span data-ttu-id="edf28-166">String</span><span class="sxs-lookup"><span data-stu-id="edf28-166">String</span></span>| <span data-ttu-id="edf28-167">O endereço SMTP do contato, por exemplo, "jeff@contoso.onmicrosoft.com".</span><span class="sxs-lookup"><span data-stu-id="edf28-167">The SMTP address for the contact, for example, "jeff@contoso.onmicrosoft.com".</span></span> |
| <span data-ttu-id="edf28-168">mailNickname</span><span class="sxs-lookup"><span data-stu-id="edf28-168">mailNickname</span></span>                 | <span data-ttu-id="edf28-169">String</span><span class="sxs-lookup"><span data-stu-id="edf28-169">String</span></span>                                                     | <span data-ttu-id="edf28-170">Alias de email (parte do endereço de email, esperando o símbolo @) desse contato organizacional.</span><span class="sxs-lookup"><span data-stu-id="edf28-170">Email alias (portion of email address pre-pending the @ symbol) for this organizational contact.</span></span>                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="edf28-171">onPremisesLastSyncDateTime</span><span class="sxs-lookup"><span data-stu-id="edf28-171">onPremisesLastSyncDateTime</span></span>   | <span data-ttu-id="edf28-172">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="edf28-172">DateTimeOffset</span></span>                                             | <span data-ttu-id="edf28-173">Data e hora da última sincronização do contato organizacional do AD local.</span><span class="sxs-lookup"><span data-stu-id="edf28-173">Date and time when this organizational contact was last synchronized from on-premises AD.</span></span> <span data-ttu-id="edf28-174">Essas informações de data e hora usam o formato ISO 8601 e está sempre no horário UTC.</span><span class="sxs-lookup"><span data-stu-id="edf28-174">This date and time information uses ISO 8601 format and is always in UTC time.</span></span> <span data-ttu-id="edf28-175">Por exemplo, meia-noite em UTC no dia 1º de janeiro de 2014 teria esta aparência: '2014-01-01T00:00:00Z'.</span><span class="sxs-lookup"><span data-stu-id="edf28-175">For example, midnight UTC on Jan 1, 2014 would look like this: '2014-01-01T00:00:00Z'.</span></span>   |
| <span data-ttu-id="edf28-176">onPremisesProvisioningErrors</span><span class="sxs-lookup"><span data-stu-id="edf28-176">onPremisesProvisioningErrors</span></span> |<span data-ttu-id="edf28-177">coleção [OnPremisesProvisioningError](onpremisesprovisioningerror.md)</span><span class="sxs-lookup"><span data-stu-id="edf28-177">[onPremisesProvisioningError](onpremisesprovisioningerror.md) collection</span></span>       | <span data-ttu-id="edf28-178">Lista de erros de provisionamento de sincronização para este contato organizacional.</span><span class="sxs-lookup"><span data-stu-id="edf28-178">List of any synchronization provisioning errors for this organizational contact.</span></span>                                                                                                                                                                                                                                                                                                |
|<span data-ttu-id="edf28-179">onPremisesSyncEnabled</span><span class="sxs-lookup"><span data-stu-id="edf28-179">onPremisesSyncEnabled</span></span>|<span data-ttu-id="edf28-180">Booliano</span><span class="sxs-lookup"><span data-stu-id="edf28-180">Boolean</span></span>|<span data-ttu-id="edf28-181">**true** se esse objeto for sincronizado a partir de um diretório local; **false** se esse objeto foi originalmente sincronizado a partir de um diretório local, mas não é mais sincronizado e agora é Mastered no Exchange; **NULL** se esse objeto nunca tiver sido sincronizado a partir de um diretório local (padrão).</span><span class="sxs-lookup"><span data-stu-id="edf28-181">**true** if this object is synced from an on-premises directory; **false** if this object was originally synced from an on-premises directory but is no longer synced and now mastered in Exchange; **null** if this object has never been synced from an on-premises directory (default).</span></span>|
| <span data-ttu-id="edf28-182">telefones</span><span class="sxs-lookup"><span data-stu-id="edf28-182">phones</span></span>                       | <span data-ttu-id="edf28-183">Coleção [phone](phone.md)</span><span class="sxs-lookup"><span data-stu-id="edf28-183">[phone](phone.md) collection</span></span>                            | <span data-ttu-id="edf28-184">Lista de telefones para este contato organizacional.</span><span class="sxs-lookup"><span data-stu-id="edf28-184">List of phones for this organizational contact.</span></span> <span data-ttu-id="edf28-185">Os tipos de telefone podem ser móveis, de negócios e de businessFax.</span><span class="sxs-lookup"><span data-stu-id="edf28-185">Phone types can be mobile, business, and businessFax.</span></span> <span data-ttu-id="edf28-186">Somente um de cada tipo pode estar presente na coleção.</span><span class="sxs-lookup"><span data-stu-id="edf28-186">Only one of each type can ever be present in the collection.</span></span>                                                                                                                       |
| <span data-ttu-id="edf28-187">proxyAddresses</span><span class="sxs-lookup"><span data-stu-id="edf28-187">proxyAddresses</span></span>               | <span data-ttu-id="edf28-188">Coleção de cadeias de caracteres</span><span class="sxs-lookup"><span data-stu-id="edf28-188">String collection</span></span>                                         | <span data-ttu-id="edf28-189">Por exemplo: "SMTP: bob@contoso.com", "SMTP: bob@sales.contoso.com".</span><span class="sxs-lookup"><span data-stu-id="edf28-189">For example: "SMTP: bob@contoso.com", "smtp: bob@sales.contoso.com".</span></span> <span data-ttu-id="edf28-190">O operador **any** é obrigatório para expressões de filtro em propriedades de vários valores.</span><span class="sxs-lookup"><span data-stu-id="edf28-190">The **any** operator is required for filter expressions on multi-valued properties.</span></span> <span data-ttu-id="edf28-191">Oferece \$suporte a filtro.</span><span class="sxs-lookup"><span data-stu-id="edf28-191">Supports \$filter.</span></span>                                                                                                                                                                               |
| <span data-ttu-id="edf28-192">surname</span><span class="sxs-lookup"><span data-stu-id="edf28-192">surname</span></span>                      | <span data-ttu-id="edf28-193">String</span><span class="sxs-lookup"><span data-stu-id="edf28-193">String</span></span>                                                     | <span data-ttu-id="edf28-194">Sobrenome para este contato organizacional.</span><span class="sxs-lookup"><span data-stu-id="edf28-194">Last name for this organizational contact.</span></span>                          |

## <a name="relationships"></a><span data-ttu-id="edf28-195">Relações</span><span class="sxs-lookup"><span data-stu-id="edf28-195">Relationships</span></span>

| <span data-ttu-id="edf28-196">Relação</span><span class="sxs-lookup"><span data-stu-id="edf28-196">Relationship</span></span> | <span data-ttu-id="edf28-197">Tipo</span><span class="sxs-lookup"><span data-stu-id="edf28-197">Type</span></span>   |<span data-ttu-id="edf28-198">Descrição</span><span class="sxs-lookup"><span data-stu-id="edf28-198">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="edf28-199">directReports</span><span class="sxs-lookup"><span data-stu-id="edf28-199">directReports</span></span>|<span data-ttu-id="edf28-200">Coleção [directoryObject](directoryobject.md)</span><span class="sxs-lookup"><span data-stu-id="edf28-200">[directoryObject](directoryobject.md) collection</span></span>| <span data-ttu-id="edf28-201">Os subordinados diretos do contato.</span><span class="sxs-lookup"><span data-stu-id="edf28-201">The contact's direct reports.</span></span> <span data-ttu-id="edf28-202">(Os usuários e contatos que têm a propriedade do gerente definidas para este contato.)  Somente leitura.</span><span class="sxs-lookup"><span data-stu-id="edf28-202">(The users and contacts that have their manager property set to this contact.)  Read-only.</span></span> <span data-ttu-id="edf28-203">Anulável.</span><span class="sxs-lookup"><span data-stu-id="edf28-203">Nullable.</span></span>|
|<span data-ttu-id="edf28-204">manager</span><span class="sxs-lookup"><span data-stu-id="edf28-204">manager</span></span>|[<span data-ttu-id="edf28-205">directoryObject</span><span class="sxs-lookup"><span data-stu-id="edf28-205">directoryObject</span></span>](directoryobject.md)| <span data-ttu-id="edf28-206">O usuário ou contato que é o gerente do contato.</span><span class="sxs-lookup"><span data-stu-id="edf28-206">The user or contact that is this contact's manager.</span></span> <span data-ttu-id="edf28-207">Somente leitura.</span><span class="sxs-lookup"><span data-stu-id="edf28-207">Read-only.</span></span>|
|<span data-ttu-id="edf28-208">memberOf</span><span class="sxs-lookup"><span data-stu-id="edf28-208">memberOf</span></span>|<span data-ttu-id="edf28-209">Coleção [directoryObject](directoryobject.md)</span><span class="sxs-lookup"><span data-stu-id="edf28-209">[directoryObject](directoryobject.md) collection</span></span>| <span data-ttu-id="edf28-210">Grupos dos quais este contato é membro.</span><span class="sxs-lookup"><span data-stu-id="edf28-210">Groups that this contact is a member of.</span></span> <span data-ttu-id="edf28-211">Somente leitura.</span><span class="sxs-lookup"><span data-stu-id="edf28-211">Read-only.</span></span> <span data-ttu-id="edf28-212">Anulável.</span><span class="sxs-lookup"><span data-stu-id="edf28-212">Nullable.</span></span>|
|<span data-ttu-id="edf28-213">transitiveMemberOf</span><span class="sxs-lookup"><span data-stu-id="edf28-213">transitiveMemberOf</span></span>|<span data-ttu-id="edf28-214">Coleção [directoryObject](directoryobject.md)</span><span class="sxs-lookup"><span data-stu-id="edf28-214">[directoryObject](directoryobject.md) collection</span></span>| <span data-ttu-id="edf28-215">Grupos dos quais este contato é membro, incluindo grupos nos quais o contato está aninhado.</span><span class="sxs-lookup"><span data-stu-id="edf28-215">Groups that this contact is a member of, including groups that the contact is nested under.</span></span>|<span data-ttu-id="edf28-216">.</span><span class="sxs-lookup"><span data-stu-id="edf28-216"></span></span> <span data-ttu-id="edf28-217">Somente leitura.</span><span class="sxs-lookup"><span data-stu-id="edf28-217">Read-only.</span></span> <span data-ttu-id="edf28-218">Anulável.</span><span class="sxs-lookup"><span data-stu-id="edf28-218">Nullable.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="edf28-219">Representação JSON</span><span class="sxs-lookup"><span data-stu-id="edf28-219">JSON representation</span></span>

<span data-ttu-id="edf28-220">Veja a seguir uma representação JSON do recurso</span><span class="sxs-lookup"><span data-stu-id="edf28-220">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "directReports",
    "manager",
    "memberOf"
  ],
  "keyProperty": "id",
  "baseType":"microsoft.graph.entity",  
  "@odata.type": "microsoft.graph.orgcontact"
}-->

```json
{
  "addresses": [{"@odata.type": "microsoft.graph.physicalOfficeAddress"}],
  "companyName": "string",
  "department": "string",
  "displayName": "string",
  "givenName": "string",
  "id": "string (identifier)",
  "jobTitle": "string",
  "mail": "string",
  "mailNickname": "string",
  "onPremisesLastSyncDateTime": "string (timestamp)",
  "onPremisesProvisioningErrors": [{"@odata.type": "microsoft.graph.onPremisesProvisioningError"}],
  "onPremisesSyncEnabled": true,
  "phones": [{"@odata.type": "microsoft.graph.phone"}],
  "proxyAddresses": ["string"],
  "surname": "string"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "orgContact resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->