---
title: Criar conversa
description: 'Crie uma nova conversa incluindo um thread e uma postagem. '
author: yyuank
localization_priority: Normal
ms.prod: groups
doc_type: apiPageType
ms.openlocfilehash: d72280e295f69a03267a25138f2d6e44151695af
ms.sourcegitcommit: 258974d689cb8f04ff542ec8bc5fe5793da5cc05
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/08/2020
ms.locfileid: "48385797"
---
# <a name="create-conversation"></a>Criar conversa

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Crie uma nova [conversa](../resources/conversation.md) incluindo um thread e uma postagem. 

Use [reply thread](conversationthread-reply.md) ou [reply post](post-reply.md) para postar mais na conversa.

## <a name="permissions"></a>Permissões
Uma das seguintes permissões é obrigatória para chamar esta API. Para saber mais, incluindo como escolher permissões, confira [Permissões](/graph/permissions-reference).

|Tipo de permissão      | Permissões (da com menos para a com mais privilégios)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (conta corporativa ou de estudante) | Group.ReadWrite.All    |
|Delegado (conta pessoal da Microsoft) | Sem suporte.    |
|Aplicativo | Sem suporte. |

## <a name="http-request"></a>Solicitação HTTP
<!-- { "blockType": "ignored" } -->
```http
POST /groups/{id}/conversations
```

## <a name="request-headers"></a>Cabeçalhos de solicitação
| Cabeçalho       | Valor |
|:---------------|:--------|
| Autorização  | {token} de portador. Obrigatório.  |
| Content-Type  | application/json  |

## <a name="request-body"></a>Corpo da solicitação
No corpo da solicitação, forneça uma representação JSON do objeto [conversation](../resources/conversation.md) que contém um [conversationThread](../resources/conversationthread.md) e um [post](../resources/post.md).

## <a name="response"></a>Resposta
Se bem-sucedido, este método retorna um código de resposta `201 Created` e um objeto [conversation](../resources/conversation.md) no corpo da resposta. 

A resposta inclui as IDs da nova conversa e do thread, que você pode usar na operação [listar postagens](conversationthread-list-posts.md) para obter a nova postagem também.

## <a name="example"></a>Exemplo
#### <a name="request"></a>Solicitação
Este é um exemplo de solicitação.

<!-- {
  "blockType": "ignored",
  "name": "create_conversation_from_group"
}-->
```http
POST https://graph.microsoft.com/beta/groups/29981b6a-0e57-42dc-94c9-cd24f5306196/conversations
Content-type: application/json

{
  "topic":"New head count",
  "threads":[
    {
      "posts":[
        {
          "body":{
            "contentType":"html",
            "content":"The confirmation will come by the end of the week."
          },
          "newParticipants":[
            {
              "emailAddress":{
                "name":"Adele Vance",
                "address":"AdeleV@contoso.onmicrosoft.com"
              }
            }
          ]
        }
      ]
    }
  ]
}
```

#### <a name="response"></a>Resposta
Este é um exemplo de resposta.
>**Observação:**  o objeto de resposta mostrado aqui pode ser encurtado por questões de legibilidade. Todas as propriedades serão retornadas de uma chamada real.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.conversation"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "@odata.context":"https://graph.microsoft.com/beta/$metadata#groups('29981b6a-0e57-42dc-94c9-cd24f5306196')/conversations/$entity",
  "id":"AAQkADPxBgqECsrFDTuM=",
  "threads@odata.context":"https://graph.microsoft.com/beta/$metadata#groups('29981b6a-0e57-42dc-94c9-cd24f5306196')/conversations('AAQkADPxBgqECsrFDTuM%3D')/threads",
  "threads":[
    {
      "id":"AAQkADUNO4xAAMbGA93Sw-EGCoQKysUNO4w=="
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "Create Conversation",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
  ]
}
-->


