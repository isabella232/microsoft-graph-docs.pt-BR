---
title: 'openShiftChangeRequest: recusar'
description: Recusar uma solicitação de openshift.
localization_priority: Normal
author: akumar39
ms.prod: microsoft-teams
doc_type: apiPageType
ms.openlocfilehash: 9fa98977d06d2eb3e1f2993779f2390bc364780c
ms.sourcegitcommit: 2ddc63c889fc2f4666aa55bca7ce0221ab899abf
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/07/2019
ms.locfileid: "39895544"
---
# <a name="openshiftchangerequest-decline"></a><span data-ttu-id="7cc7e-103">openShiftChangeRequest: recusar</span><span class="sxs-lookup"><span data-stu-id="7cc7e-103">openShiftChangeRequest: decline</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="7cc7e-104">Recusar um objeto [openshiftchangerequest](../resources/openshiftchangerequest.md) .</span><span class="sxs-lookup"><span data-stu-id="7cc7e-104">Decline an [openshiftchangerequest](../resources/openshiftchangerequest.md) object.</span></span>

## <a name="permissions"></a><span data-ttu-id="7cc7e-105">Permissões</span><span class="sxs-lookup"><span data-stu-id="7cc7e-105">Permissions</span></span>

<span data-ttu-id="7cc7e-p101">Uma das seguintes permissões é obrigatória para chamar esta API. Para saber mais, incluindo como escolher permissões, confira [Permissões](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="7cc7e-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="7cc7e-108">Tipo de permissão</span><span class="sxs-lookup"><span data-stu-id="7cc7e-108">Permission type</span></span>                        | <span data-ttu-id="7cc7e-109">Permissões (da com menos para a com mais privilégios)</span><span class="sxs-lookup"><span data-stu-id="7cc7e-109">Permissions (from least to most privileged)</span></span> |
|:---------------------------------------|:--------------------------------------------|
| <span data-ttu-id="7cc7e-110">Delegado (conta corporativa ou de estudante)</span><span class="sxs-lookup"><span data-stu-id="7cc7e-110">Delegated (work or school account)</span></span>     | <span data-ttu-id="7cc7e-111">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="7cc7e-111">Group.ReadWrite.All</span></span> |
| <span data-ttu-id="7cc7e-112">Delegado (conta pessoal da Microsoft)</span><span class="sxs-lookup"><span data-stu-id="7cc7e-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="7cc7e-113">Sem suporte.</span><span class="sxs-lookup"><span data-stu-id="7cc7e-113">Not supported.</span></span> |
| <span data-ttu-id="7cc7e-114">Aplicativo</span><span class="sxs-lookup"><span data-stu-id="7cc7e-114">Application</span></span>                            | <span data-ttu-id="7cc7e-115">Sem suporte.</span><span class="sxs-lookup"><span data-stu-id="7cc7e-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="7cc7e-116">Solicitação HTTP</span><span class="sxs-lookup"><span data-stu-id="7cc7e-116">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
POST /teams/{id}/schedule/openShiftsChangeRequests/decline
```

## <a name="request-headers"></a><span data-ttu-id="7cc7e-117">Cabeçalhos de solicitação</span><span class="sxs-lookup"><span data-stu-id="7cc7e-117">Request headers</span></span>

| <span data-ttu-id="7cc7e-118">Nome</span><span class="sxs-lookup"><span data-stu-id="7cc7e-118">Name</span></span>          | <span data-ttu-id="7cc7e-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="7cc7e-119">Description</span></span>   |
|:--------------|:--------------|
| <span data-ttu-id="7cc7e-120">Autorização</span><span class="sxs-lookup"><span data-stu-id="7cc7e-120">Authorization</span></span> | <span data-ttu-id="7cc7e-p102">{token} de portador. Obrigatório.</span><span class="sxs-lookup"><span data-stu-id="7cc7e-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="7cc7e-123">Corpo da solicitação</span><span class="sxs-lookup"><span data-stu-id="7cc7e-123">Request body</span></span>

<span data-ttu-id="7cc7e-124">Forneça um objeto JSON com os seguintes parâmetros no corpo da solicitação.</span><span class="sxs-lookup"><span data-stu-id="7cc7e-124">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="7cc7e-125">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="7cc7e-125">Parameter</span></span>    | <span data-ttu-id="7cc7e-126">Tipo</span><span class="sxs-lookup"><span data-stu-id="7cc7e-126">Type</span></span>        | <span data-ttu-id="7cc7e-127">Descrição</span><span class="sxs-lookup"><span data-stu-id="7cc7e-127">Description</span></span> |
|:-------------|:------------|:------------|
|<span data-ttu-id="7cc7e-128">mensagem</span><span class="sxs-lookup"><span data-stu-id="7cc7e-128">message</span></span>|<span data-ttu-id="7cc7e-129">String</span><span class="sxs-lookup"><span data-stu-id="7cc7e-129">String</span></span>|<span data-ttu-id="7cc7e-130">Uma mensagem de recusa personalizada.</span><span class="sxs-lookup"><span data-stu-id="7cc7e-130">A custom decline message.</span></span>|

## <a name="response"></a><span data-ttu-id="7cc7e-131">Resposta</span><span class="sxs-lookup"><span data-stu-id="7cc7e-131">Response</span></span>

<span data-ttu-id="7cc7e-p103">Se bem-sucedido, este método retorna um código de resposta `200 OK`. Não retorna nada no corpo da resposta.</span><span class="sxs-lookup"><span data-stu-id="7cc7e-p103">If successful, this method returns a `200 OK` response code. It does not return anything in the response body.</span></span>

## <a name="examples"></a><span data-ttu-id="7cc7e-134">Exemplos</span><span class="sxs-lookup"><span data-stu-id="7cc7e-134">Examples</span></span>

<span data-ttu-id="7cc7e-135">O exemplo a seguir mostra como chamar essa API.</span><span class="sxs-lookup"><span data-stu-id="7cc7e-135">The following example shows how to call this API.</span></span>

### <a name="request"></a><span data-ttu-id="7cc7e-136">Solicitação</span><span class="sxs-lookup"><span data-stu-id="7cc7e-136">Request</span></span>

<span data-ttu-id="7cc7e-137">Este é um exemplo de solicitação.</span><span class="sxs-lookup"><span data-stu-id="7cc7e-137">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "openshiftchangerequest_decline"
}-->

```http
POST https://graph.microsoft.com/beta/teams/{id}/schedule/openShiftsChangeRequests/decline
Content-type: application/json

{
  "message": "message-value"
}
```

### <a name="response"></a><span data-ttu-id="7cc7e-138">Resposta</span><span class="sxs-lookup"><span data-stu-id="7cc7e-138">Response</span></span>

<span data-ttu-id="7cc7e-139">Este é um exemplo de resposta.</span><span class="sxs-lookup"><span data-stu-id="7cc7e-139">The following is an example of the response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.None"
} -->

```http
HTTP/1.1 200 OK
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "openShiftChangeRequest: decline",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->