---
title: Excluir certificateBasedAuthConfiguration
description: Exclua certificateBasedAuthConfiguration.
localization_priority: Normal
author: davidmu1
ms.prod: microsoft-identity-platform
doc_type: apiPageType
ms.openlocfilehash: 113823fcb19014255b8334fb88f6a9f897eace8b
ms.sourcegitcommit: c9b9ff2c862f8d96d282a7bdf641cdb9c53a4600
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/22/2019
ms.locfileid: "37632557"
---
# <a name="delete-certificatebasedauthconfiguration"></a><span data-ttu-id="e1bb5-103">Excluir certificateBasedAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="e1bb5-103">Delete certificateBasedAuthConfiguration</span></span>

<span data-ttu-id="e1bb5-104">Excluir um objeto [certificateBasedAuthConfiguration](../resources/certificateBasedAuthConfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="e1bb5-104">Delete a [certificateBasedAuthConfiguration](../resources/certificateBasedAuthConfiguration.md) object.</span></span>

## <a name="permissions"></a><span data-ttu-id="e1bb5-105">Permissões</span><span class="sxs-lookup"><span data-stu-id="e1bb5-105">Permissions</span></span>

<span data-ttu-id="e1bb5-p101">Uma das seguintes permissões é obrigatória para chamar esta API. Para saber mais, incluindo como escolher permissões, confira [Permissões](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="e1bb5-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="e1bb5-108">Tipo de permissão</span><span class="sxs-lookup"><span data-stu-id="e1bb5-108">Permission type</span></span>                        | <span data-ttu-id="e1bb5-109">Permissões (da com menos para a com mais privilégios)</span><span class="sxs-lookup"><span data-stu-id="e1bb5-109">Permissions (from least to most privileged)</span></span> |
|:---------------------------------------|:--------------------------------------------|
| <span data-ttu-id="e1bb5-110">Delegado (conta corporativa ou de estudante)</span><span class="sxs-lookup"><span data-stu-id="e1bb5-110">Delegated (work or school account)</span></span>     | <span data-ttu-id="e1bb5-111">Organization.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e1bb5-111">Organization.ReadWrite.All</span></span> |
| <span data-ttu-id="e1bb5-112">Delegado (conta pessoal da Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e1bb5-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="e1bb5-113">Sem suporte.</span><span class="sxs-lookup"><span data-stu-id="e1bb5-113">Not supported.</span></span> |
| <span data-ttu-id="e1bb5-114">Aplicativo</span><span class="sxs-lookup"><span data-stu-id="e1bb5-114">Application</span></span>    | <span data-ttu-id="e1bb5-115">Organization.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e1bb5-115">Organization.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="e1bb5-116">Solicitação HTTP</span><span class="sxs-lookup"><span data-stu-id="e1bb5-116">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
DELETE /organization/{id}/certificateBasedAuthConfiguration/{id}
```

## <a name="request-headers"></a><span data-ttu-id="e1bb5-117">Cabeçalhos de solicitação</span><span class="sxs-lookup"><span data-stu-id="e1bb5-117">Request headers</span></span>

| <span data-ttu-id="e1bb5-118">Nome</span><span class="sxs-lookup"><span data-stu-id="e1bb5-118">Name</span></span>          | <span data-ttu-id="e1bb5-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="e1bb5-119">Description</span></span>   |
|:--------------|:--------------|
| <span data-ttu-id="e1bb5-120">Autorização</span><span class="sxs-lookup"><span data-stu-id="e1bb5-120">Authorization</span></span> | <span data-ttu-id="e1bb5-p102">{token} de portador. Obrigatório.</span><span class="sxs-lookup"><span data-stu-id="e1bb5-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="e1bb5-123">Corpo da solicitação</span><span class="sxs-lookup"><span data-stu-id="e1bb5-123">Request body</span></span>

<span data-ttu-id="e1bb5-124">Não forneça um corpo de solicitação para esse método.</span><span class="sxs-lookup"><span data-stu-id="e1bb5-124">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="e1bb5-125">Resposta</span><span class="sxs-lookup"><span data-stu-id="e1bb5-125">Response</span></span>

<span data-ttu-id="e1bb5-p103">Se bem-sucedido, este método retorna um código de resposta `204 No Content`. Não retorna nada no corpo da resposta.</span><span class="sxs-lookup"><span data-stu-id="e1bb5-p103">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="examples"></a><span data-ttu-id="e1bb5-128">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e1bb5-128">Examples</span></span>

### <a name="request"></a><span data-ttu-id="e1bb5-129">Solicitação</span><span class="sxs-lookup"><span data-stu-id="e1bb5-129">Request</span></span>

<span data-ttu-id="e1bb5-130">Este é um exemplo de solicitação.</span><span class="sxs-lookup"><span data-stu-id="e1bb5-130">The following is an example of the request.</span></span>

# <a name="httptabhttp"></a>[<span data-ttu-id="e1bb5-131">HTTP</span><span class="sxs-lookup"><span data-stu-id="e1bb5-131">HTTP</span></span>](#tab/http)
<!-- {
  "blockType": "request",
  "name": "delete_certificatebasedauthconfiguration"
}-->

```http
DELETE https://graph.microsoft.com/v1.0/organization/{id}/certificateBasedAuthConfiguration/{id}
```
# <a name="ctabcsharp"></a>[<span data-ttu-id="e1bb5-132">C#</span><span class="sxs-lookup"><span data-stu-id="e1bb5-132">C#</span></span>](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/delete-certificatebasedauthconfiguration-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javascripttabjavascript"></a>[<span data-ttu-id="e1bb5-133">JavaScript</span><span class="sxs-lookup"><span data-stu-id="e1bb5-133">JavaScript</span></span>](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/delete-certificatebasedauthconfiguration-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="objective-ctabobjc"></a>[<span data-ttu-id="e1bb5-134">Objective-C</span><span class="sxs-lookup"><span data-stu-id="e1bb5-134">Objective-C</span></span>](#tab/objc)
[!INCLUDE [sample-code](../includes/snippets/objc/delete-certificatebasedauthconfiguration-objc-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javatabjava"></a>[<span data-ttu-id="e1bb5-135">Java</span><span class="sxs-lookup"><span data-stu-id="e1bb5-135">Java</span></span>](#tab/java)
[!INCLUDE [sample-code](../includes/snippets/java/delete-certificatebasedauthconfiguration-java-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---


### <a name="response"></a><span data-ttu-id="e1bb5-136">Resposta</span><span class="sxs-lookup"><span data-stu-id="e1bb5-136">Response</span></span>

<span data-ttu-id="e1bb5-137">Este é um exemplo de resposta.</span><span class="sxs-lookup"><span data-stu-id="e1bb5-137">The following is an example of the response.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true
} -->

```http
HTTP/1.1 204 No Content
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Delete certificateBasedAuthConfiguration",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->