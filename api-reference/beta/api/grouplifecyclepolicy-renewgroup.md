---
title: 'groupLifecyclePolicy: renovar'
description: Renovar a expiração de um grupo. Após renovar um grupo, o período de validade é estendido de acordo com o número de dias definido na política.
localization_priority: Normal
author: yyuank
ms.prod: groups
doc_type: apiPageType
ms.openlocfilehash: 009186a210b29b541b7ee7eff8ddbbdcb397827d
ms.sourcegitcommit: 342516a52b69fcda31442b130eb6bd7e2c8a0066
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/10/2020
ms.locfileid: "48953587"
---
# <a name="grouplifecyclepolicy-renewgroup"></a>groupLifecyclePolicy: renovar

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Renovar a expiração de um grupo. Após renovar um grupo, o período de validade é estendido de acordo com o número de dias definido na política.

> **Observação:** Ao chamar o ponto de extremidade v 1.0, use o método [renovar grupo](/graph/api/group-renew?view=graph-rest-1.0) .

## <a name="permissions"></a>Permissões

Uma das seguintes permissões é obrigatória para chamar esta API. Para saber mais, incluindo como escolher permissões, confira [Permissões](/graph/permissions-reference).
 

|Tipo de permissão      | Permissões (da com menos para a com mais privilégios)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (conta corporativa ou de estudante) | Group.ReadWrite.All ou Directory.ReadWrite.All    |
|Delegado (conta pessoal da Microsoft) | Sem suporte |
|Aplicativo | Group.ReadWrite.All ou Directory.ReadWrite.All |

## <a name="http-request"></a>Solicitação HTTP
<!-- { "blockType": "ignored" } -->
```http
POST /groupLifecyclePolicies/renewGroup

```

## <a name="request-headers"></a>Cabeçalhos de solicitação

| Nome | Descrição |
|:---------------|:----------|
| Autorização | {token} de portador. Obrigatório. |
| Content-Type  | application/json |

## <a name="request-body"></a>Corpo da solicitação
Forneça um objeto JSON com os seguintes parâmetros no corpo da solicitação.

| Parâmetro | Tipo | Descrição |
|:---------------|:--------|:----------|
|groupId|Guid| A ID do grupo a ser renovado. |

## <a name="response"></a>Resposta

Se bem-sucedido, este método retorna um código de resposta `204 No Content`. Não retorna nada no corpo da resposta.

## <a name="example"></a>Exemplo

##### <a name="request"></a>Solicitação


# <a name="http"></a>[HTTP](#tab/http)
<!-- {
  "blockType": "request",
  "name": "grouplifecyclepolicy_renewgroup"
}-->
```http
POST https://graph.microsoft.com/beta/groupLifecyclePolicies/renewGroup
Content-type: application/json
Content-length: 57

{
  "groupId": "ffffffff-ffff-ffff-ffff-ffffffffffff"
}
```
# <a name="c"></a>[C#](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/grouplifecyclepolicy-renewgroup-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javascript"></a>[JavaScript](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/grouplifecyclepolicy-renewgroup-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="objective-c"></a>[Objective-C](#tab/objc)
[!INCLUDE [sample-code](../includes/snippets/objc/grouplifecyclepolicy-renewgroup-objc-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="java"></a>[Java](#tab/java)
[!INCLUDE [sample-code](../includes/snippets/java/grouplifecyclepolicy-renewgroup-java-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---


##### <a name="response"></a>Resposta

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.None"
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "groupLifecyclePolicy: renewgroup",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
  ]
}
-->
