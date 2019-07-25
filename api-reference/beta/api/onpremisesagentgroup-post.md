---
title: Criar onPremisesAgentGroup
description: Criar um novo objeto **onPremisesAgentGroup** .
localization_priority: Normal
author: davidmu1
ms.prod: microsoft-identity-platform
doc_type: apiPageType
ms.openlocfilehash: 752081e6b50460e8185f4bddddce603bf54e5d86
ms.sourcegitcommit: 8844023e15b7649a5c03603aee243acf85930ef2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/24/2019
ms.locfileid: "35841091"
---
# <a name="create-onpremisesagentgroup"></a><span data-ttu-id="fa731-103">Criar onPremisesAgentGroup</span><span class="sxs-lookup"><span data-stu-id="fa731-103">Create onPremisesAgentGroup</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="fa731-104">Criar um novo objeto [onPremisesAgentGroup](../resources/onpremisesagentgroup.md) .</span><span class="sxs-lookup"><span data-stu-id="fa731-104">Create a new [onPremisesAgentGroup](../resources/onpremisesagentgroup.md) object.</span></span>

## <a name="permissions"></a><span data-ttu-id="fa731-105">Permissões</span><span class="sxs-lookup"><span data-stu-id="fa731-105">Permissions</span></span>

<span data-ttu-id="fa731-p101">Uma das seguintes permissões é obrigatória para chamar esta API. Para saber mais, incluindo como escolher permissões, confira [Permissões](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="fa731-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="fa731-108">Tipo de permissão</span><span class="sxs-lookup"><span data-stu-id="fa731-108">Permission type</span></span>                        | <span data-ttu-id="fa731-109">Permissões (da com menos para a com mais privilégios)</span><span class="sxs-lookup"><span data-stu-id="fa731-109">Permissions (from least to most privileged)</span></span> |
|:--------------------------------------|:---------------------------------------------------------|
|<span data-ttu-id="fa731-110">Delegado (conta corporativa ou de estudante)</span><span class="sxs-lookup"><span data-stu-id="fa731-110">Delegated (work or school account)</span></span>     | <span data-ttu-id="fa731-111">OnPremisesPublishingProfiles. ReadWrite. All</span><span class="sxs-lookup"><span data-stu-id="fa731-111">OnPremisesPublishingProfiles.ReadWrite.All</span></span> |
| <span data-ttu-id="fa731-112">Delegado (conta pessoal da Microsoft)</span><span class="sxs-lookup"><span data-stu-id="fa731-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="fa731-113">Sem suporte.</span><span class="sxs-lookup"><span data-stu-id="fa731-113">Not supported.</span></span> |
| <span data-ttu-id="fa731-114">Aplicativo</span><span class="sxs-lookup"><span data-stu-id="fa731-114">Application</span></span>                            | <span data-ttu-id="fa731-115">Sem suporte.</span><span class="sxs-lookup"><span data-stu-id="fa731-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="fa731-116">Solicitação HTTP</span><span class="sxs-lookup"><span data-stu-id="fa731-116">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
POST ~/onPremisesPublishingProfiles/{publishingType}/agentGroups/{id}/agents
```

## <a name="request-headers"></a><span data-ttu-id="fa731-117">Cabeçalhos de solicitação</span><span class="sxs-lookup"><span data-stu-id="fa731-117">Request headers</span></span>

| <span data-ttu-id="fa731-118">Nome</span><span class="sxs-lookup"><span data-stu-id="fa731-118">Name</span></span>          | <span data-ttu-id="fa731-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="fa731-119">Description</span></span>   |
|:--------------|:--------------|
| <span data-ttu-id="fa731-120">Autorização</span><span class="sxs-lookup"><span data-stu-id="fa731-120">Authorization</span></span> | <span data-ttu-id="fa731-121">Portador {token}</span><span class="sxs-lookup"><span data-stu-id="fa731-121">Bearer {token}</span></span> |

## <a name="request-body"></a><span data-ttu-id="fa731-122">Corpo da solicitação</span><span class="sxs-lookup"><span data-stu-id="fa731-122">Request body</span></span>

<span data-ttu-id="fa731-123">No corpo da solicitação, forneça uma representação JSON de um objeto [onPremisesAgentGroup](../resources/onpremisesagentgroup.md) .</span><span class="sxs-lookup"><span data-stu-id="fa731-123">In the request body, supply a JSON representation of an [onPremisesAgentGroup](../resources/onpremisesagentgroup.md) object.</span></span>

```json
{
    "displayName": "New Group"
}
```

## <a name="response"></a><span data-ttu-id="fa731-124">Resposta</span><span class="sxs-lookup"><span data-stu-id="fa731-124">Response</span></span>

<span data-ttu-id="fa731-125">Se tiver êxito, este método retornará `201 Created` um código de resposta e um objeto [onPremisesAgentGroup](../resources/onpremisesagentgroup.md) no corpo da resposta.</span><span class="sxs-lookup"><span data-stu-id="fa731-125">If successful, this method returns a `201 Created` response code and an [onPremisesAgentGroup](../resources/onpremisesagentgroup.md) object in the response body.</span></span>

## <a name="examples"></a><span data-ttu-id="fa731-126">Exemplos</span><span class="sxs-lookup"><span data-stu-id="fa731-126">Examples</span></span>

### <a name="request"></a><span data-ttu-id="fa731-127">Solicitação</span><span class="sxs-lookup"><span data-stu-id="fa731-127">Request</span></span>

<span data-ttu-id="fa731-128">Este é um exemplo de solicitação.</span><span class="sxs-lookup"><span data-stu-id="fa731-128">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_onpremisesagent_from_onpremisesagentgroup"
}-->

```http
POST https://graph.microsoft.com/beta/onPremisesPublishingProfiles/provisioning/agentGroups
```

<span data-ttu-id="fa731-129">No corpo da solicitação, forneça uma representação JSON do objeto [onPremisesAgentGroup](../resources/onpremisesagentgroup.md) .</span><span class="sxs-lookup"><span data-stu-id="fa731-129">In the request body, supply a JSON representation of [onPremisesAgentGroup](../resources/onpremisesagentgroup.md) object.</span></span>

```json
{
    "displayName": "New Group"
}
```

### <a name="response"></a><span data-ttu-id="fa731-130">Resposta</span><span class="sxs-lookup"><span data-stu-id="fa731-130">Response</span></span>

<span data-ttu-id="fa731-131">Este é um exemplo de resposta.</span><span class="sxs-lookup"><span data-stu-id="fa731-131">The following is an example of the response.</span></span>

> <span data-ttu-id="fa731-p102">**Observação:** o objeto response mostrado aqui pode ser encurtado para legibilidade. Todas as propriedades serão retornadas de uma chamada real.</span><span class="sxs-lookup"><span data-stu-id="fa731-p102">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.onPremisesAgentGroup"
} -->

```http
HTTP/1.1 201 Created
Content-type: application/json

{
    "id": "4655ed41-1619-4848-92bb-0576d3038682",
    "displayName": "New Group",
    "publishingType": "provisioning",
    "isDefault": false
}
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create onPremisesAgent",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->