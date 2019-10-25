---
title: Listar políticas
description: Recupere uma lista de objetos conditionalAccessPolicy.
localization_priority: Normal
author: davidmu1
ms.prod: microsoft-identity-platform
doc_type: apiPageType
ms.openlocfilehash: 1a7400eddd8d3b238437cbd65d4b413ef1cc5096
ms.sourcegitcommit: 3ee6a3a949be7f0a9028bde90092a10a42e0f1fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/23/2019
ms.locfileid: "37638418"
---
# <a name="list-policies"></a><span data-ttu-id="acb00-103">Listar políticas</span><span class="sxs-lookup"><span data-stu-id="acb00-103">List policies</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="acb00-104">Recupere uma lista de objetos [conditionalAccessPolicy](../resources/conditionalaccesspolicy.md) .</span><span class="sxs-lookup"><span data-stu-id="acb00-104">Retrieve a list of [conditionalAccessPolicy](../resources/conditionalaccesspolicy.md) objects.</span></span>

## <a name="permissions"></a><span data-ttu-id="acb00-105">Permissões</span><span class="sxs-lookup"><span data-stu-id="acb00-105">Permissions</span></span>

<span data-ttu-id="acb00-p101">Uma das seguintes permissões é obrigatória para chamar esta API. Para saber mais, incluindo como escolher permissões, confira [Permissões](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="acb00-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="acb00-108">Tipo de permissão</span><span class="sxs-lookup"><span data-stu-id="acb00-108">Permission type</span></span>                        | <span data-ttu-id="acb00-109">Permissões (da com menos para a com mais privilégios)</span><span class="sxs-lookup"><span data-stu-id="acb00-109">Permissions (from least to most privileged)</span></span>                                       |
|:--------------------------------------|:----------------------------------------------------------------------------------|
|<span data-ttu-id="acb00-110">Delegado (conta corporativa ou de estudante)</span><span class="sxs-lookup"><span data-stu-id="acb00-110">Delegated (work or school account)</span></span>     | <span data-ttu-id="acb00-111">Policy.Read.All</span><span class="sxs-lookup"><span data-stu-id="acb00-111">Policy.Read.All</span></span> |
|<span data-ttu-id="acb00-112">Delegado (conta pessoal da Microsoft)</span><span class="sxs-lookup"><span data-stu-id="acb00-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="acb00-113">Sem suporte.</span><span class="sxs-lookup"><span data-stu-id="acb00-113">Not supported.</span></span> |
|<span data-ttu-id="acb00-114">Aplicativo</span><span class="sxs-lookup"><span data-stu-id="acb00-114">Application</span></span>                            | <span data-ttu-id="acb00-115">Sem suporte.</span><span class="sxs-lookup"><span data-stu-id="acb00-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="acb00-116">Solicitação HTTP</span><span class="sxs-lookup"><span data-stu-id="acb00-116">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
GET /conditionalAccess/policies
```

## <a name="optional-query-parameters"></a><span data-ttu-id="acb00-117">Parâmetros de consulta opcionais</span><span class="sxs-lookup"><span data-stu-id="acb00-117">Optional query parameters</span></span>

<span data-ttu-id="acb00-118">Este método oferece suporte `$skip`aos `$top`parâmetros `$count`de `$filter`consulta `$orderBy`do, `$select` ,,, e OData para ajudar a personalizar a resposta.</span><span class="sxs-lookup"><span data-stu-id="acb00-118">This method supports the `$skip`, `$top`, `$count`, `$filter`, `$orderBy`, and `$select` OData query parameters to help customize the response.</span></span> <span data-ttu-id="acb00-119">Para obter informações gerais, confira [parâmetros de consulta OData](/graph/query-parameters).</span><span class="sxs-lookup"><span data-stu-id="acb00-119">For general information, see [OData query parameters](/graph/query-parameters).</span></span>

## <a name="request-headers"></a><span data-ttu-id="acb00-120">Cabeçalhos de solicitação</span><span class="sxs-lookup"><span data-stu-id="acb00-120">Request headers</span></span>

| <span data-ttu-id="acb00-121">Nome</span><span class="sxs-lookup"><span data-stu-id="acb00-121">Name</span></span>      |<span data-ttu-id="acb00-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="acb00-122">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="acb00-123">Autorização</span><span class="sxs-lookup"><span data-stu-id="acb00-123">Authorization</span></span> | <span data-ttu-id="acb00-124">Portador {token}</span><span class="sxs-lookup"><span data-stu-id="acb00-124">Bearer {token}</span></span> |

## <a name="request-body"></a><span data-ttu-id="acb00-125">Corpo da solicitação</span><span class="sxs-lookup"><span data-stu-id="acb00-125">Request body</span></span>

<span data-ttu-id="acb00-126">Não forneça um corpo de solicitação para esse método.</span><span class="sxs-lookup"><span data-stu-id="acb00-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="acb00-127">Resposta</span><span class="sxs-lookup"><span data-stu-id="acb00-127">Response</span></span>

<span data-ttu-id="acb00-128">Se tiver êxito, este método retornará `200 OK` um código de resposta e uma coleção de objetos [conditionalAccessPolicy](../resources/conditionalaccesspolicy.md) no corpo da resposta.</span><span class="sxs-lookup"><span data-stu-id="acb00-128">If successful, this method returns a `200 OK` response code and a collection of [conditionalAccessPolicy](../resources/conditionalaccesspolicy.md) objects in the response body.</span></span>

## <a name="examples"></a><span data-ttu-id="acb00-129">Exemplos</span><span class="sxs-lookup"><span data-stu-id="acb00-129">Examples</span></span>

### <a name="request"></a><span data-ttu-id="acb00-130">Solicitação</span><span class="sxs-lookup"><span data-stu-id="acb00-130">Request</span></span>

<span data-ttu-id="acb00-131">Este é um exemplo de solicitação.</span><span class="sxs-lookup"><span data-stu-id="acb00-131">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_policies"
}-->

```http
GET https://graph.microsoft.com/beta/conditionalAccess/policies?$filter=displayName eq 'SimplePolicy1' or displayName eq 'SimplePolicy2'
```

### <a name="response"></a><span data-ttu-id="acb00-132">Resposta</span><span class="sxs-lookup"><span data-stu-id="acb00-132">Response</span></span>

<span data-ttu-id="acb00-133">Este é um exemplo de resposta.</span><span class="sxs-lookup"><span data-stu-id="acb00-133">The following is an example of the response.</span></span>

> <span data-ttu-id="acb00-p103">**Observação:** o objeto response mostrado aqui pode ser encurtado para legibilidade. Todas as propriedades serão retornadas de uma chamada real.</span><span class="sxs-lookup"><span data-stu-id="acb00-p103">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": false,
  "@odata.type": "microsoft.graph.conditionalAccessPolicy",
  "isCollection": true
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json


{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#conditionalAccess/policies",
    "value": [
        {
            "id": "ad8d2b4a-8d30-413f-88b8-144c6c8d98d9",
            "displayName": "SimplePolicy1",
            "createdDateTime": null,
            "modifiedDateTime": null,
            "state": "disabled",
            "sessionControls": null,
            "conditions": {
                "signInRiskLevels": [],
                "clientAppTypes": [],
                "platforms": null,
                "locations": null,
                "deviceStates": null,
                "applications": {
                    "includeApplications": [
                        "None"
                    ],
                    "excludeApplications": [],
                    "includeUserActions": []
                },
                "users": {
                    "includeUsers": [
                        "None"
                    ],
                    "excludeUsers": [],
                    "includeGroups": [],
                    "excludeGroups": [],
                    "includeRoles": [],
                    "excludeRoles": []
                }
            },
            "grantControls": {
                "operator": "OR",
                "builtInControls": [
                    "block"
                ],
                "customAuthenticationFactors": [],
                "termsOfUse": []
            }
        },
        {
            "id": "c558e346-969d-40a7-a64e-2df6c2c88490",
            "displayName": "SimplePolicy2",
            "createdDateTime": null,
            "modifiedDateTime": null,
            "state": "disabled",
            "sessionControls": null,
            "conditions": {
                "signInRiskLevels": [],
                "clientAppTypes": [],
                "platforms": null,
                "locations": null,
                "deviceStates": null,
                "applications": {
                    "includeApplications": [
                        "None"
                    ],
                    "excludeApplications": [],
                    "includeUserActions": []
                },
                "users": {
                    "includeUsers": [
                        "None"
                    ],
                    "excludeUsers": [],
                    "includeGroups": [],
                    "excludeGroups": [],
                    "includeRoles": [],
                    "excludeRoles": []
                }
            },
            "grantControls": {
                "operator": "OR",
                "builtInControls": [
                    "mfa"
                ],
                "customAuthenticationFactors": [],
                "termsOfUse": []
            }
        }
    ]
}
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List policies",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->