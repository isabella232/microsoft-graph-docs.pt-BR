---
title: Obter namedLocation
description: Recupere as propriedades e os relacionamentos de um objeto namedlocation.
localization_priority: Normal
author: davidmu1
ms.prod: microsoft-identity-platform
doc_type: apiPageType
ms.openlocfilehash: 9c69a2ed2ae1418f2c7b338487f8e53ba5568a5f
ms.sourcegitcommit: d189830649794365464e37539e02239f883011da
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/24/2019
ms.locfileid: "37653675"
---
# <a name="get-namedlocation"></a><span data-ttu-id="54688-103">Obter namedLocation</span><span class="sxs-lookup"><span data-stu-id="54688-103">Get namedLocation</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="54688-104">Recupere as propriedades e os relacionamentos de um objeto [namedLocation](../resources/namedlocation.md) .</span><span class="sxs-lookup"><span data-stu-id="54688-104">Retrieve the properties and relationships of a [namedLocation](../resources/namedlocation.md) object.</span></span>

## <a name="permissions"></a><span data-ttu-id="54688-105">Permissões</span><span class="sxs-lookup"><span data-stu-id="54688-105">Permissions</span></span>

<span data-ttu-id="54688-p101">Uma das seguintes permissões é obrigatória para chamar esta API. Para saber mais, incluindo como escolher permissões, confira [Permissões](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="54688-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="54688-108">Tipo de permissão</span><span class="sxs-lookup"><span data-stu-id="54688-108">Permission type</span></span>                        | <span data-ttu-id="54688-109">Permissões (da com menos para a com mais privilégios)</span><span class="sxs-lookup"><span data-stu-id="54688-109">Permissions (from least to most privileged)</span></span> |
|:---------------------------------------|:--------------------------------------------|
| <span data-ttu-id="54688-110">Delegado (conta corporativa ou de estudante)</span><span class="sxs-lookup"><span data-stu-id="54688-110">Delegated (work or school account)</span></span>     | <span data-ttu-id="54688-111">Policy.Read.All</span><span class="sxs-lookup"><span data-stu-id="54688-111">Policy.Read.All</span></span> |
| <span data-ttu-id="54688-112">Delegado (conta pessoal da Microsoft)</span><span class="sxs-lookup"><span data-stu-id="54688-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="54688-113">Sem suporte.</span><span class="sxs-lookup"><span data-stu-id="54688-113">Not supported.</span></span> |
| <span data-ttu-id="54688-114">Aplicativo</span><span class="sxs-lookup"><span data-stu-id="54688-114">Application</span></span>                            | <span data-ttu-id="54688-115">Sem suporte.</span><span class="sxs-lookup"><span data-stu-id="54688-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="54688-116">Solicitação HTTP</span><span class="sxs-lookup"><span data-stu-id="54688-116">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
GET /conditionalAccess/namedLocations/{id}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="54688-117">Parâmetros de consulta opcionais</span><span class="sxs-lookup"><span data-stu-id="54688-117">Optional query parameters</span></span>

<span data-ttu-id="54688-118">Este método oferece suporte `select` ao parâmetro de consulta OData para ajudar a personalizar a resposta.</span><span class="sxs-lookup"><span data-stu-id="54688-118">This method supports the `select` OData query parameter to help customize the response.</span></span> <span data-ttu-id="54688-119">Para obter informações gerais, confira [parâmetros de consulta OData](/graph/query-parameters).</span><span class="sxs-lookup"><span data-stu-id="54688-119">For general information, see [OData query parameters](/graph/query-parameters).</span></span>

## <a name="request-headers"></a><span data-ttu-id="54688-120">Cabeçalhos de solicitação</span><span class="sxs-lookup"><span data-stu-id="54688-120">Request headers</span></span>

| <span data-ttu-id="54688-121">Nome</span><span class="sxs-lookup"><span data-stu-id="54688-121">Name</span></span>      |<span data-ttu-id="54688-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="54688-122">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="54688-123">Autorização</span><span class="sxs-lookup"><span data-stu-id="54688-123">Authorization</span></span> | <span data-ttu-id="54688-p103">{token} de portador. Obrigatório.</span><span class="sxs-lookup"><span data-stu-id="54688-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="54688-126">Corpo da solicitação</span><span class="sxs-lookup"><span data-stu-id="54688-126">Request body</span></span>

<span data-ttu-id="54688-127">Não forneça um corpo de solicitação para esse método.</span><span class="sxs-lookup"><span data-stu-id="54688-127">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="54688-128">Resposta</span><span class="sxs-lookup"><span data-stu-id="54688-128">Response</span></span>

<span data-ttu-id="54688-129">Se tiver êxito, este método retornará `200 OK` um código de resposta e o objeto [namedLocation](../resources/namedlocation.md) solicitado no corpo da resposta.</span><span class="sxs-lookup"><span data-stu-id="54688-129">If successful, this method returns a `200 OK` response code and the requested [namedLocation](../resources/namedlocation.md) object in the response body.</span></span>

## <a name="examples"></a><span data-ttu-id="54688-130">Exemplos</span><span class="sxs-lookup"><span data-stu-id="54688-130">Examples</span></span>

### <a name="request"></a><span data-ttu-id="54688-131">Solicitação</span><span class="sxs-lookup"><span data-stu-id="54688-131">Request</span></span>

<span data-ttu-id="54688-132">Este é um exemplo de solicitação.</span><span class="sxs-lookup"><span data-stu-id="54688-132">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_namedlocation"
}-->

```http
GET https://graph.microsoft.com/beta/conditionalAccess/namedLocations/0854951d-5fc0-4eb1-b392-9b2c9d7949c2
```

### <a name="response"></a><span data-ttu-id="54688-133">Resposta</span><span class="sxs-lookup"><span data-stu-id="54688-133">Response</span></span>

<span data-ttu-id="54688-134">Este é um exemplo de resposta.</span><span class="sxs-lookup"><span data-stu-id="54688-134">The following is an example of the response.</span></span>

> <span data-ttu-id="54688-p104">**Observação:** o objeto response mostrado aqui pode ser encurtado para legibilidade. Todas as propriedades serão retornadas de uma chamada real.</span><span class="sxs-lookup"><span data-stu-id="54688-p104">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.namedLocation"
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#namedLocations/$entity",
    "@odata.type": "#microsoft.graph.ipNamedLocation",
    "id": "0854951d-5fc0-4eb1-b392-9b2c9d7949c2",
    "displayName": "Untrusted IP named location",
    "modifiedDateTime": "2019-09-04T01:11:34.9387578Z",
    "createdDateTime": "2019-09-04T01:11:34.9387578Z",
    "isTrusted": false,
    "ipRanges": [
        {
            "@odata.type": "#microsoft.graph.iPv4CidrRange",
            "cidrAddress": "12.34.221.11/22"
        },
        {
            "@odata.type": "#microsoft.graph.iPv6CidrRange",
            "cidrAddress": "2001:0:9d38:90d6:0:0:0:0/63"
        }
    ]
}
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get namedLocation",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->