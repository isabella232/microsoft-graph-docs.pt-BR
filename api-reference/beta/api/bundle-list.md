---
author: JeremyKelley
ms.author: jeremyke
title: Listar pacotes
description: Listar os pacotes na unidade de um usuário
localization_priority: Normal
ms.prod: sharepoint
ms.openlocfilehash: b3191418a9d82f0961e920400d74fd429d3febc9
ms.sourcegitcommit: 56c0b609dfb1bc5d900956f407d107cdab7086e8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/30/2019
ms.locfileid: "35932597"
---
# <a name="list-bundles"></a><span data-ttu-id="89b3e-103">Listar pacotes</span><span class="sxs-lookup"><span data-stu-id="89b3e-103">List bundles</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="89b3e-104">Obter uma lista de todos os pacotes de [pacote][] na unidade de um usuário.</span><span class="sxs-lookup"><span data-stu-id="89b3e-104">Get a list of all the [bundles][bundle] in a user's drive.</span></span>

## <a name="permissions"></a><span data-ttu-id="89b3e-105">Permissões</span><span class="sxs-lookup"><span data-stu-id="89b3e-105">Permissions</span></span>

<span data-ttu-id="89b3e-p101">Uma das seguintes permissões é obrigatória para chamar esta API. Para saber mais, incluindo como escolher permissões, confira [Permissões](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="89b3e-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="89b3e-108">Tipo de permissão</span><span class="sxs-lookup"><span data-stu-id="89b3e-108">Permission type</span></span>      | <span data-ttu-id="89b3e-109">Permissões (da com menos para a com mais privilégios)</span><span class="sxs-lookup"><span data-stu-id="89b3e-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="89b3e-110">Delegado (conta corporativa ou de estudante)</span><span class="sxs-lookup"><span data-stu-id="89b3e-110">Delegated (work or school account)</span></span> | <span data-ttu-id="89b3e-111">Sem suporte.</span><span class="sxs-lookup"><span data-stu-id="89b3e-111">Not supported.</span></span>                             |
|<span data-ttu-id="89b3e-112">Delegado (conta pessoal da Microsoft)</span><span class="sxs-lookup"><span data-stu-id="89b3e-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="89b3e-113">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="89b3e-113">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All</span></span>    |
|<span data-ttu-id="89b3e-114">Aplicativo</span><span class="sxs-lookup"><span data-stu-id="89b3e-114">Application</span></span>          | <span data-ttu-id="89b3e-115">Sem suporte.</span><span class="sxs-lookup"><span data-stu-id="89b3e-115">Not supported.</span></span>                                           |

## <a name="http-request"></a><span data-ttu-id="89b3e-116">Solicitação HTTP</span><span class="sxs-lookup"><span data-stu-id="89b3e-116">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
GET /drive/bundles
```

## <a name="optional-query-parameters"></a><span data-ttu-id="89b3e-117">Parâmetros de consulta opcionais</span><span class="sxs-lookup"><span data-stu-id="89b3e-117">Optional query parameters</span></span>

<span data-ttu-id="89b3e-118">Esse método dá suporte a [Parâmetros de consulta OData][] para filtrar e dar forma à resposta.</span><span class="sxs-lookup"><span data-stu-id="89b3e-118">This method supports the [OData Query Parameters][] to filter and shape the response.</span></span>

<span data-ttu-id="89b3e-119">Você não pode usar `expand=children` o parâmetro de consulta ao enumerar os pacotes.</span><span class="sxs-lookup"><span data-stu-id="89b3e-119">You can't use the `expand=children` query parameter when enumerating bundles.</span></span>

## <a name="request-headers"></a><span data-ttu-id="89b3e-120">Cabeçalhos de solicitação</span><span class="sxs-lookup"><span data-stu-id="89b3e-120">Request headers</span></span>

| <span data-ttu-id="89b3e-121">Nome</span><span class="sxs-lookup"><span data-stu-id="89b3e-121">Name</span></span>          | <span data-ttu-id="89b3e-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="89b3e-122">Description</span></span>  |
|:------------- |:------------ |
| <span data-ttu-id="89b3e-123">Autorização</span><span class="sxs-lookup"><span data-stu-id="89b3e-123">Authorization</span></span> | <span data-ttu-id="89b3e-124">\{token\} de portador.</span><span class="sxs-lookup"><span data-stu-id="89b3e-124">Bearer \{token\}.</span></span> <span data-ttu-id="89b3e-125">Obrigatório.</span><span class="sxs-lookup"><span data-stu-id="89b3e-125">Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="89b3e-126">Corpo da solicitação</span><span class="sxs-lookup"><span data-stu-id="89b3e-126">Request body</span></span>

<span data-ttu-id="89b3e-127">Não forneça um corpo de solicitação com esse método.</span><span class="sxs-lookup"><span data-stu-id="89b3e-127">Do not supply a request body with this method.</span></span>

## <a name="response"></a><span data-ttu-id="89b3e-128">Resposta</span><span class="sxs-lookup"><span data-stu-id="89b3e-128">Response</span></span>

<span data-ttu-id="89b3e-129">Se tiver êxito, essa solicitação retornará a lista de itens de pacote definidos para a unidade.</span><span class="sxs-lookup"><span data-stu-id="89b3e-129">If successful, this request returns the list of bundle items defined for the drive.</span></span>

<span data-ttu-id="89b3e-130">Leia o tópico [respostas de erro][error-response] para obter mais informações sobre como os erros são retornados.</span><span class="sxs-lookup"><span data-stu-id="89b3e-130">Read the [Error Responses][error-response] topic for more info about how errors are returned.</span></span>

## <a name="examples"></a><span data-ttu-id="89b3e-131">Exemplos</span><span class="sxs-lookup"><span data-stu-id="89b3e-131">Examples</span></span>

### <a name="example-1-list-all-bundles-in-a-drive"></a><span data-ttu-id="89b3e-132">Exemplo 1: listar todos os pacotes em uma unidade</span><span class="sxs-lookup"><span data-stu-id="89b3e-132">Example 1: List all bundles in a drive</span></span>

<span data-ttu-id="89b3e-133">Para solicitar uma enumeração de todos os pacotes definidos na unidade, você pode fazer uma solicitação para a coleção de **pacotes** sem qualquer parâmetro.</span><span class="sxs-lookup"><span data-stu-id="89b3e-133">To request an enumeration of all bundles defined in the drive, you can make a request to the **bundles** collection without any parameters.</span></span>

#### <a name="request"></a><span data-ttu-id="89b3e-134">Solicitação</span><span class="sxs-lookup"><span data-stu-id="89b3e-134">Request</span></span>


# <a name="httptabhttp"></a>[<span data-ttu-id="89b3e-135">HTTP</span><span class="sxs-lookup"><span data-stu-id="89b3e-135">HTTP</span></span>](#tab/http)
<!-- { "blockType": "request", "name": "list-all-bundles", "tags": "service.onedrive" } -->

```http
GET https://graph.microsoft.com/beta/drive/bundles
```
# <a name="ctabcsharp"></a>[<span data-ttu-id="89b3e-136">C#</span><span class="sxs-lookup"><span data-stu-id="89b3e-136">C#</span></span>](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/list-all-bundles-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javascripttabjavascript"></a>[<span data-ttu-id="89b3e-137">Javascript</span><span class="sxs-lookup"><span data-stu-id="89b3e-137">Javascript</span></span>](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/list-all-bundles-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="objective-ctabobjc"></a>[<span data-ttu-id="89b3e-138">Objetivo-C</span><span class="sxs-lookup"><span data-stu-id="89b3e-138">Objective-C</span></span>](#tab/objc)
[!INCLUDE [sample-code](../includes/snippets/objc/list-all-bundles-objc-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javatabjava"></a>[<span data-ttu-id="89b3e-139">Java</span><span class="sxs-lookup"><span data-stu-id="89b3e-139">Java</span></span>](#tab/java)
[!INCLUDE [sample-code](../includes/snippets/java/list-all-bundles-java-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---


#### <a name="response"></a><span data-ttu-id="89b3e-140">Resposta</span><span class="sxs-lookup"><span data-stu-id="89b3e-140">Response</span></span>

<!-- { "blockType": "response", "@odata.type": "microsoft.graph.driveItem", "truncated": true, "isCollection": true } -->

```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "value": [
    {
      "id": "0123456789abc",
      "name": "Vacation photo album",
      "bundle": {
        "childCount": 1,
        "album": { }
      }
    },
    {
      "id": "0120310201abd",
      "name": "Family shared files",
      "bundle": {
        "childCount": 1
      }
    }
  ],
  "@odata.nextLink": "https://..."
}
```

<span data-ttu-id="89b3e-141">O objeto de resposta mostrado aqui pode ser reduzido para legibilidade.</span><span class="sxs-lookup"><span data-stu-id="89b3e-141">The response object shown here might be shortened for readability.</span></span> <span data-ttu-id="89b3e-142">Todas as propriedades serão retornadas de uma chamada real.</span><span class="sxs-lookup"><span data-stu-id="89b3e-142">All the properties will be returned from an actual call.</span></span>


### <a name="example-2-list-all-photo-albums-in-a-drive"></a><span data-ttu-id="89b3e-143">Exemplo 2: listar todos os álbuns de fotos em uma unidade</span><span class="sxs-lookup"><span data-stu-id="89b3e-143">Example 2: List all photo albums in a drive</span></span>

<span data-ttu-id="89b3e-144">Para filtrar a lista de pacotes retornados de uma solicitação para a coleção de pacotes, você pode usar o `filter` parâmetro de cadeia de caracteres de consulta para especificar o tipo de pacote a ser retornado verificando a existência de uma faceta no pacote:</span><span class="sxs-lookup"><span data-stu-id="89b3e-144">To filter the list of bundles returned from a request to the bundles collection, you can use the `filter` query string parameter to specify the type of bundle to return by checking for the existence of a facet on the bundle:</span></span>

#### <a name="request"></a><span data-ttu-id="89b3e-145">Solicitação</span><span class="sxs-lookup"><span data-stu-id="89b3e-145">Request</span></span>


# <a name="httptabhttp"></a>[<span data-ttu-id="89b3e-146">HTTP</span><span class="sxs-lookup"><span data-stu-id="89b3e-146">HTTP</span></span>](#tab/http)
<!-- {"blockType": "request", "name": "list-album-bundles", "tags": "service.onedrive" } -->

```http
GET https://graph.microsoft.com/beta/drive/bundles?filter=bundle/album%20ne%20null
```
# <a name="ctabcsharp"></a>[<span data-ttu-id="89b3e-147">C#</span><span class="sxs-lookup"><span data-stu-id="89b3e-147">C#</span></span>](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/list-album-bundles-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javascripttabjavascript"></a>[<span data-ttu-id="89b3e-148">Javascript</span><span class="sxs-lookup"><span data-stu-id="89b3e-148">Javascript</span></span>](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/list-album-bundles-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="objective-ctabobjc"></a>[<span data-ttu-id="89b3e-149">Objetivo-C</span><span class="sxs-lookup"><span data-stu-id="89b3e-149">Objective-C</span></span>](#tab/objc)
[!INCLUDE [sample-code](../includes/snippets/objc/list-album-bundles-objc-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javatabjava"></a>[<span data-ttu-id="89b3e-150">Java</span><span class="sxs-lookup"><span data-stu-id="89b3e-150">Java</span></span>](#tab/java)
[!INCLUDE [sample-code](../includes/snippets/java/list-album-bundles-java-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---


#### <a name="response"></a><span data-ttu-id="89b3e-151">Resposta</span><span class="sxs-lookup"><span data-stu-id="89b3e-151">Response</span></span>

<span data-ttu-id="89b3e-152">A resposta para um GET para o ponto de extremidade de pacotes é uma matriz de recursos do [driveItem][] com o [pacote][].</span><span class="sxs-lookup"><span data-stu-id="89b3e-152">The response to a GET to the bundles endpoint is an array of [driveItem][] resources with the [bundle][].</span></span>
<span data-ttu-id="89b3e-153">Como todos os pacotes são itens, você pode usar todas as operações de item padrão neles.</span><span class="sxs-lookup"><span data-stu-id="89b3e-153">Because all bundles are items, you can use use all the standard item operations on them.</span></span>

<!-- { "blockType": "response", "@odata.type": "microsoft.graph.driveItem", "truncated": true, "isCollection": true } -->

```json
HTTP/1.1 200 OK
Content-type: application/json

{
  "value": [
    {
      "id": "0123456789abc",
      "name": "Vacation photo album",
      "bundle": {
        "childCount": 1,
        "album": { }
      }
    },
    {
      "id": "120301010abcd",
      "name": "Seattle Center event",
      "bundle": {
        "childCount": 4,
        "album": { }
      },
      "tags": [
        {
          "name": "outside",
          "autoTagged": { }
        }
      ]
    }
  ]
}
```

<span data-ttu-id="89b3e-154">O objeto de resposta mostrado aqui pode ser reduzido para legibilidade.</span><span class="sxs-lookup"><span data-stu-id="89b3e-154">The response object shown here might be shortened for readability.</span></span> <span data-ttu-id="89b3e-155">Todas as propriedades serão retornadas de uma chamada real.</span><span class="sxs-lookup"><span data-stu-id="89b3e-155">All the properties will be returned from an actual call.</span></span>


[pacote]: ../resources/bundle.md
[bundle]: ../resources/bundle.md
[driveItem]: ../resources/driveItem.md
[error-response]: /graph/errors
[Parâmetros de consulta OData]: /graph/query-parameters
[OData Query Parameters]: /graph/query-parameters

<!-- {
  "type": "#page.annotation",
  "description": "List the bundles in a drive.",
  "keywords": "list,bundle,collection",
  "section": "documentation",
  "tocPath": "Bundles/List"
} -->