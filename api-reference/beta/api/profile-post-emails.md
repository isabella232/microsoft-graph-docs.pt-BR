---
title: Criar email
description: Criar um novo email.
localization_priority: Normal
author: kevinbellinger
ms.prod: people
doc_type: apiPageType
ms.openlocfilehash: 25f81760c4d4320474027d0f3d7f5113007ae94d
ms.sourcegitcommit: 62507617292d5ad8598e83a8a253c986d9bac787
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2019
ms.locfileid: "37937704"
---
# <a name="create-itememail"></a>Criar email

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Criar um novo [email](../resources/itememail.md).

## <a name="permissions"></a>Permissões

Uma das seguintes permissões é obrigatória para chamar esta API. Para saber mais, incluindo como escolher permissões, confira [Permissões](/graph/permissions-reference).

| Tipo de permissão                        | Permissões (da com menos para a com mais privilégios) |
|:---------------------------------------|:--------------------------------------------|
| Delegado (conta corporativa ou de estudante)     | User. ReadWrite, User. ReadWrite. All |
| Delegado (conta pessoal da Microsoft) | User. ReadWrite, User. ReadWrite. All |
| Aplicativo                            | User.ReadWrite.All |

## <a name="http-request"></a>Solicitação HTTP

<!-- { "blockType": "ignored" } -->

```http
POST /user/profile/emails
```

## <a name="request-headers"></a>Cabeçalhos de solicitação

| Nome      |Descrição|
|:----------|:----------|
| Autorização  | {token} de portador. Obrigatório.|
| Content-Type   | application/json. Obrigatório. |

## <a name="request-body"></a>Corpo da solicitação

No corpo da solicitação, forneça uma representação JSON de um objeto de [email](../resources/itememail.md) .

## <a name="response"></a>Resposta

Se tiver êxito, este método retornará `201 Created` um código de resposta e um novo objeto de [email](../resources/itememail.md) no corpo da resposta.

## <a name="examples"></a>Exemplos

### <a name="request"></a>Solicitação

Este é um exemplo de solicitação.
<!-- {
  "blockType": "request",
  "name": "create_itememail_from_profile"
}-->

```http
POST https://graph.microsoft.com/beta/user/profile/emails
Content-type: application/json

{
  "address": "address-value",
  "displayName": "displayName-value",
  "type": "type-value"
}
```

### <a name="response"></a>Resposta

Este é um exemplo de resposta.

> **Observação:** o objeto response mostrado aqui pode ser encurtado para legibilidade. Todas as propriedades serão retornadas de uma chamada real.

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.itemEmail"
} -->

```http
HTTP/1.1 201 Created
Content-type: application/json

{
  "address": "address-value",
  "displayName": "displayName-value",
  "type": "type-value"
}
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create itemEmail",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->