---
title: 'Grupo: checkMemberObjects'
description: Verifique se há associação em uma lista de grupos ou funções de diretório para o objeto de grupo especificado.
localization_priority: Normal
author: davidmu1
ms.prod: microsoft-identity-platform
doc_type: apiPageType
ms.openlocfilehash: e4f6bb2f940cd32940391799ff4a93387ab8ac32
ms.sourcegitcommit: c25828c596b7e0939fa164a3d7754722943152c2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/21/2019
ms.locfileid: "38757301"
---
# <a name="group-checkmemberobjects"></a><span data-ttu-id="7b5d4-103">Grupo: checkMemberObjects</span><span class="sxs-lookup"><span data-stu-id="7b5d4-103">group: checkMemberObjects</span></span>

<span data-ttu-id="7b5d4-104">Verifique se há associação em uma lista de grupos ou funções de diretório para o grupo especificado.</span><span class="sxs-lookup"><span data-stu-id="7b5d4-104">Check for membership in a list of groups or directory roles for the specified group.</span></span> <span data-ttu-id="7b5d4-105">Este método é transitivo.</span><span class="sxs-lookup"><span data-stu-id="7b5d4-105">This method is transitive.</span></span>

## <a name="permissions"></a><span data-ttu-id="7b5d4-106">Permissões</span><span class="sxs-lookup"><span data-stu-id="7b5d4-106">Permissions</span></span>

<span data-ttu-id="7b5d4-p102">Uma das seguintes permissões é obrigatória para chamar esta API. Para saber mais, incluindo como escolher permissões, confira [Permissões](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="7b5d4-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="7b5d4-109">Tipo de permissão</span><span class="sxs-lookup"><span data-stu-id="7b5d4-109">Permission type</span></span>                        | <span data-ttu-id="7b5d4-110">Permissões (da com menos para a com mais privilégios)</span><span class="sxs-lookup"><span data-stu-id="7b5d4-110">Permissions (from least to most privileged)</span></span> |
|:---------------------------------------|:--------------------------------------------|
| <span data-ttu-id="7b5d4-111">Delegado (conta corporativa ou de estudante)</span><span class="sxs-lookup"><span data-stu-id="7b5d4-111">Delegated (work or school account)</span></span>     | <span data-ttu-id="7b5d4-112">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="7b5d4-112">Group.Read.All, Group.ReadWrite.All</span></span><br><span data-ttu-id="7b5d4-113">E</span><span class="sxs-lookup"><span data-stu-id="7b5d4-113">And:</span></span><br><ul><li><span data-ttu-id="7b5d4-114">Se estiver verificando a associação em unidades administrativas: AdministrativeUnit. Read. All, AdministrativeUnit. ReadWrite. All</span><span class="sxs-lookup"><span data-stu-id="7b5d4-114">If checking for membership in administrative units: AdministrativeUnit.Read.All, AdministrativeUnit.ReadWrite.All</span></span></li></ul><br><span data-ttu-id="7b5d4-115">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="7b5d4-115">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span> |
| <span data-ttu-id="7b5d4-116">Delegado (conta pessoal da Microsoft)</span><span class="sxs-lookup"><span data-stu-id="7b5d4-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="7b5d4-117">Sem suporte.</span><span class="sxs-lookup"><span data-stu-id="7b5d4-117">Not supported.</span></span> |
| <span data-ttu-id="7b5d4-118">Aplicativo</span><span class="sxs-lookup"><span data-stu-id="7b5d4-118">Application</span></span>                            | <span data-ttu-id="7b5d4-119">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="7b5d4-119">Group.Read.All, Group.ReadWrite.All</span></span><br><span data-ttu-id="7b5d4-120">E</span><span class="sxs-lookup"><span data-stu-id="7b5d4-120">And:</span></span><br><ul><li><span data-ttu-id="7b5d4-121">Se estiver verificando a associação em unidades administrativas: AdministrativeUnit. Read. All, AdministrativeUnit. ReadWrite. All</span><span class="sxs-lookup"><span data-stu-id="7b5d4-121">If checking for membership in administrative units: AdministrativeUnit.Read.All, AdministrativeUnit.ReadWrite.All</span></span></ul></li><br><span data-ttu-id="7b5d4-122">Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="7b5d4-122">Directory.Read.All, Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="7b5d4-123">Solicitação HTTP</span><span class="sxs-lookup"><span data-stu-id="7b5d4-123">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
POST /groups/{id}/checkMemberObjects
```

## <a name="request-headers"></a><span data-ttu-id="7b5d4-124">Cabeçalhos de solicitação</span><span class="sxs-lookup"><span data-stu-id="7b5d4-124">Request headers</span></span>

| <span data-ttu-id="7b5d4-125">Nome</span><span class="sxs-lookup"><span data-stu-id="7b5d4-125">Name</span></span>          | <span data-ttu-id="7b5d4-126">Descrição</span><span class="sxs-lookup"><span data-stu-id="7b5d4-126">Description</span></span>   |
|:--------------|:--------------|
| <span data-ttu-id="7b5d4-127">Autorização</span><span class="sxs-lookup"><span data-stu-id="7b5d4-127">Authorization</span></span> | <span data-ttu-id="7b5d4-p103">{token} de portador. Obrigatório.</span><span class="sxs-lookup"><span data-stu-id="7b5d4-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="7b5d4-130">Content-Type</span><span class="sxs-lookup"><span data-stu-id="7b5d4-130">Content-Type</span></span>  | <span data-ttu-id="7b5d4-p104">application/json. Obrigatório.</span><span class="sxs-lookup"><span data-stu-id="7b5d4-p104">application/json. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="7b5d4-133">Corpo da solicitação</span><span class="sxs-lookup"><span data-stu-id="7b5d4-133">Request body</span></span>

<span data-ttu-id="7b5d4-134">Forneça um objeto JSON com os seguintes parâmetros no corpo da solicitação.</span><span class="sxs-lookup"><span data-stu-id="7b5d4-134">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="7b5d4-135">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="7b5d4-135">Parameter</span></span>    | <span data-ttu-id="7b5d4-136">Tipo</span><span class="sxs-lookup"><span data-stu-id="7b5d4-136">Type</span></span>        | <span data-ttu-id="7b5d4-137">Descrição</span><span class="sxs-lookup"><span data-stu-id="7b5d4-137">Description</span></span> |
|:-------------|:------------|:------------|
|<span data-ttu-id="7b5d4-138">ids</span><span class="sxs-lookup"><span data-stu-id="7b5d4-138">ids</span></span>|<span data-ttu-id="7b5d4-139">Coleção de cadeias de caracteres</span><span class="sxs-lookup"><span data-stu-id="7b5d4-139">String collection</span></span>| <span data-ttu-id="7b5d4-140">Uma coleção que contém as IDs de objeto dos grupos, funções de diretório ou IDs RoleTemplate de funções de diretório, para verificar a associação.</span><span class="sxs-lookup"><span data-stu-id="7b5d4-140">A collection that contains the object IDs of the groups, directory roles, or roleTemplate IDs of directory roles, in which to check membership.</span></span> <span data-ttu-id="7b5d4-141">Você pode especificar até 20 objetos.</span><span class="sxs-lookup"><span data-stu-id="7b5d4-141">You can specify up to 20 objects.</span></span> |

## <a name="response"></a><span data-ttu-id="7b5d4-142">Resposta</span><span class="sxs-lookup"><span data-stu-id="7b5d4-142">Response</span></span>

<span data-ttu-id="7b5d4-143">Se tiver êxito, este método retornará `200 OK` um código de resposta e um objeto da coleção String no corpo da resposta.</span><span class="sxs-lookup"><span data-stu-id="7b5d4-143">If successful, this method returns a `200 OK` response code and a String collection object in the response body.</span></span>

## <a name="examples"></a><span data-ttu-id="7b5d4-144">Exemplos</span><span class="sxs-lookup"><span data-stu-id="7b5d4-144">Examples</span></span>

<span data-ttu-id="7b5d4-145">O exemplo a seguir mostra como chamar essa API.</span><span class="sxs-lookup"><span data-stu-id="7b5d4-145">The following example shows how to call this API.</span></span>

### <a name="request"></a><span data-ttu-id="7b5d4-146">Solicitação</span><span class="sxs-lookup"><span data-stu-id="7b5d4-146">Request</span></span>

<span data-ttu-id="7b5d4-147">Este é um exemplo de solicitação.</span><span class="sxs-lookup"><span data-stu-id="7b5d4-147">The following is an example of the request.</span></span>

# <a name="httptabhttp"></a>[<span data-ttu-id="7b5d4-148">HTTP</span><span class="sxs-lookup"><span data-stu-id="7b5d4-148">HTTP</span></span>](#tab/http)
<!-- {
  "blockType": "request",
  "name": "group_checkmemberobjects"
}-->

```http
POST https://graph.microsoft.com/v1.0/groups/{id}/checkMemberObjects
Content-type: application/json

{
  "ids": [
    "80a963dd-84af-4eb8-b2a6-781e444d4fb0",
    "62e90394-69f5-4237-9190-012177145e10",
    "86a64f51-3a64-4cc6-a8c8-6b8f000c0f52",
    "ac38546e-ddf3-437a-ac5c-27a94cd7a0f1"
  ]
}
```

### <a name="response"></a><span data-ttu-id="7b5d4-149">Resposta</span><span class="sxs-lookup"><span data-stu-id="7b5d4-149">Response</span></span>

<span data-ttu-id="7b5d4-150">Este é um exemplo de resposta.</span><span class="sxs-lookup"><span data-stu-id="7b5d4-150">The following is an example of the response.</span></span> 

> <span data-ttu-id="7b5d4-p106">**Observação:** o objeto response mostrado aqui pode ser encurtado para legibilidade. Todas as propriedades serão retornadas de uma chamada real.</span><span class="sxs-lookup"><span data-stu-id="7b5d4-p106">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "String",
  "isCollection": true
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "value": [
    "80a963dd-84af-4eb8-b2a6-781e444d4fb0", 
    "62e90394-69f5-4237-9190-012177145e10"
  ]
}
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "group: checkMemberObjects",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->