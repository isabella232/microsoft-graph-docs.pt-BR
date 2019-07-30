---
author: JeremyKelley
ms.author: jeremyke
title: Atualizar um pacote
description: Atualizar um pacote de driveItems
localization_priority: Normal
ms.prod: sharepoint
ms.openlocfilehash: bbeb9f62a0053a4735358097e2441bac08078ef7
ms.sourcegitcommit: 56c0b609dfb1bc5d900956f407d107cdab7086e8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/30/2019
ms.locfileid: "35932586"
---
# <a name="update-bundle"></a><span data-ttu-id="075fe-103">Pacote de atualização</span><span class="sxs-lookup"><span data-stu-id="075fe-103">Update bundle</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="075fe-104">Atualize os metadados de um [pacote][] de [DRIVEITEMS][driveItem] por ID.</span><span class="sxs-lookup"><span data-stu-id="075fe-104">Update the metadata for a [bundle][] of [driveItems][driveItem] by ID.</span></span>
<span data-ttu-id="075fe-105">Você só pode atualizar os seguintes metadados:</span><span class="sxs-lookup"><span data-stu-id="075fe-105">You can only update the following metadata:</span></span>

* <span data-ttu-id="075fe-106">Nome do pacote</span><span class="sxs-lookup"><span data-stu-id="075fe-106">Bundle name</span></span>
* <span data-ttu-id="075fe-107">Álbum `coverImageItemId` (se aplicável)</span><span class="sxs-lookup"><span data-stu-id="075fe-107">Album `coverImageItemId` (if applicable)</span></span>

<span data-ttu-id="075fe-108">Quaisquer outras solicitações de alteração serão ignoradas.</span><span class="sxs-lookup"><span data-stu-id="075fe-108">Any other change requests will be ignored.</span></span>

## <a name="permissions"></a><span data-ttu-id="075fe-109">Permissões</span><span class="sxs-lookup"><span data-stu-id="075fe-109">Permissions</span></span>

<span data-ttu-id="075fe-p102">Uma das seguintes permissões é obrigatória para chamar esta API. Para saber mais, incluindo como escolher permissões, confira [Permissões](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="075fe-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="075fe-112">Tipo de permissão</span><span class="sxs-lookup"><span data-stu-id="075fe-112">Permission type</span></span>      | <span data-ttu-id="075fe-113">Permissões (da com menos para a com mais privilégios)</span><span class="sxs-lookup"><span data-stu-id="075fe-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="075fe-114">Delegado (conta corporativa ou de estudante)</span><span class="sxs-lookup"><span data-stu-id="075fe-114">Delegated (work or school account)</span></span> | <span data-ttu-id="075fe-115">Sem suporte.</span><span class="sxs-lookup"><span data-stu-id="075fe-115">Not supported.</span></span>                             |
|<span data-ttu-id="075fe-116">Delegado (conta pessoal da Microsoft)</span><span class="sxs-lookup"><span data-stu-id="075fe-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="075fe-117">Files.ReadWrite, Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="075fe-117">Files.ReadWrite, Files.ReadWrite.All</span></span>   |
|<span data-ttu-id="075fe-118">Aplicativo</span><span class="sxs-lookup"><span data-stu-id="075fe-118">Application</span></span>          | <span data-ttu-id="075fe-119">Sem suporte.</span><span class="sxs-lookup"><span data-stu-id="075fe-119">Not supported.</span></span>                                           |

## <a name="http-request"></a><span data-ttu-id="075fe-120">Solicitação HTTP</span><span class="sxs-lookup"><span data-stu-id="075fe-120">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
PATCH /drive/items/{bundle-id}
```

## <a name="request-headers"></a><span data-ttu-id="075fe-121">Cabeçalhos de solicitação</span><span class="sxs-lookup"><span data-stu-id="075fe-121">Request headers</span></span>

| <span data-ttu-id="075fe-122">Nome</span><span class="sxs-lookup"><span data-stu-id="075fe-122">Name</span></span>          | <span data-ttu-id="075fe-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="075fe-123">Description</span></span>  |
|:------------- |:------------ |
| <span data-ttu-id="075fe-124">Autorização</span><span class="sxs-lookup"><span data-stu-id="075fe-124">Authorization</span></span> | <span data-ttu-id="075fe-125">\{token\} de portador.</span><span class="sxs-lookup"><span data-stu-id="075fe-125">Bearer \{token\}.</span></span> <span data-ttu-id="075fe-126">Obrigatório.</span><span class="sxs-lookup"><span data-stu-id="075fe-126">Required.</span></span> |
| <span data-ttu-id="075fe-127">if-match</span><span class="sxs-lookup"><span data-stu-id="075fe-127">if-match</span></span>      | <span data-ttu-id="075fe-128">ETag.</span><span class="sxs-lookup"><span data-stu-id="075fe-128">eTag.</span></span> <span data-ttu-id="075fe-129">Opcional.</span><span class="sxs-lookup"><span data-stu-id="075fe-129">Optional.</span></span> <span data-ttu-id="075fe-130">Se este cabeçalho de solicitação estiver incluso e a eTag fornecida não corresponder à eTag atual no buncle, uma `412 Precondition Failed` resposta será retornada.</span><span class="sxs-lookup"><span data-stu-id="075fe-130">If this request header is included and the eTag provided does not match the current eTag on the buncle, a `412 Precondition Failed` response is returned.</span></span>

## <a name="request-body"></a><span data-ttu-id="075fe-131">Corpo da solicitação</span><span class="sxs-lookup"><span data-stu-id="075fe-131">Request body</span></span>

<span data-ttu-id="075fe-132">No corpo da solicitação, forneça os valores para os campos relevantes que devem ser atualizados.</span><span class="sxs-lookup"><span data-stu-id="075fe-132">In the request body, supply the values for relevant fields that should be updated.</span></span> <span data-ttu-id="075fe-133">Propriedades existentes que não estão incluídas no corpo da solicitação terão seus valores anteriores mantidos ou serão recalculadas com base nas alterações a outros valores de propriedade.</span><span class="sxs-lookup"><span data-stu-id="075fe-133">Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values.</span></span> <span data-ttu-id="075fe-134">Para alcançar o melhor desempenho, não inclua valores existentes que não foram alterados.</span><span class="sxs-lookup"><span data-stu-id="075fe-134">For best performance, don't include existing values that haven't changed.</span></span>

## <a name="response"></a><span data-ttu-id="075fe-135">Resposta</span><span class="sxs-lookup"><span data-stu-id="075fe-135">Response</span></span>

<span data-ttu-id="075fe-136">Se tiver êxito, este método retornará um recurso [driveItem][] que representa o pacote atualizado no corpo da resposta.</span><span class="sxs-lookup"><span data-stu-id="075fe-136">If successful, this method returns a [driveItem][] resource that represents the updated bundle in the response body.</span></span>

<span data-ttu-id="075fe-137">Leia o tópico [respostas de erro][error-response] para obter mais informações sobre como os erros são retornados.</span><span class="sxs-lookup"><span data-stu-id="075fe-137">Read the [Error Responses][error-response] topic for more info about how errors are returned.</span></span>

## <a name="example"></a><span data-ttu-id="075fe-138">Exemplo</span><span class="sxs-lookup"><span data-stu-id="075fe-138">Example</span></span>

<span data-ttu-id="075fe-139">Este exemplo renomeia um pacote.</span><span class="sxs-lookup"><span data-stu-id="075fe-139">This example renames a bundle.</span></span>

### <a name="request"></a><span data-ttu-id="075fe-140">Solicitação</span><span class="sxs-lookup"><span data-stu-id="075fe-140">Request</span></span>


# <a name="httptabhttp"></a>[<span data-ttu-id="075fe-141">HTTP</span><span class="sxs-lookup"><span data-stu-id="075fe-141">HTTP</span></span>](#tab/http)
<!-- { "blockType": "request", "name": "rename-bundle" } -->

```json
PATCH https://graph.microsoft.com/beta/drive/items/{bundle-id}
Content-Type: application/json

{
  "name": "Shared legal agreements"
}
```
# <a name="ctabcsharp"></a>[<span data-ttu-id="075fe-142">C#</span><span class="sxs-lookup"><span data-stu-id="075fe-142">C#</span></span>](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/rename-bundle-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javascripttabjavascript"></a>[<span data-ttu-id="075fe-143">Javascript</span><span class="sxs-lookup"><span data-stu-id="075fe-143">Javascript</span></span>](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/rename-bundle-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="objective-ctabobjc"></a>[<span data-ttu-id="075fe-144">Objetivo-C</span><span class="sxs-lookup"><span data-stu-id="075fe-144">Objective-C</span></span>](#tab/objc)
[!INCLUDE [sample-code](../includes/snippets/objc/rename-bundle-objc-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javatabjava"></a>[<span data-ttu-id="075fe-145">Java</span><span class="sxs-lookup"><span data-stu-id="075fe-145">Java</span></span>](#tab/java)
[!INCLUDE [sample-code](../includes/snippets/java/rename-bundle-java-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---


### <a name="response"></a><span data-ttu-id="075fe-146">Resposta</span><span class="sxs-lookup"><span data-stu-id="075fe-146">Response</span></span>

<!-- { "blockType": "response", "@odata.type": "microsoft.graph.driveItem", "truncated": true } -->

```json
HTTP/1.1 200 OK
Content-Type: application/json

{
  "id": "0123456789abc",
  "name": "Shared legal agreements",
  "bundle": {
    "childCount": 3
  }
}
```

<span data-ttu-id="075fe-147">O objeto de resposta mostrado aqui pode ser reduzido para legibilidade.</span><span class="sxs-lookup"><span data-stu-id="075fe-147">The response object shown here might be shortened for readability.</span></span> <span data-ttu-id="075fe-148">Todas as propriedades serão retornadas de uma chamada real.</span><span class="sxs-lookup"><span data-stu-id="075fe-148">All the properties will be returned from an actual call.</span></span>


[pacote]: ../resources/bundle.md
[bundle]: ../resources/bundle.md
[driveItem]: ../resources/driveItem.md
[error-response]: /graph/errors

<!-- {
  "type": "#page.annotation",
  "description": "Update or replace the contents or properties of a bundle.",
  "keywords": "update,replace,contents,bundle",
  "section": "documentation",
    "tocPath": "Bundles/Update"
} -->