---
title: tipo de recurso chat
description: Um chat é uma coleção de chatMessages entre um ou mais participantes.
author: clearab
localization_priority: Normal
ms.prod: microsoft-teams
doc_type: resourcePageType
ms.openlocfilehash: da9dcf4a1777d23a3b5f4b73e505641057558605
ms.sourcegitcommit: a3fc420a5639c0f4e89af2b602db17392e176802
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/23/2020
ms.locfileid: "48222831"
---
# <a name="chat-resource-type"></a>tipo de recurso chat

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Um chat é uma coleção de [chatMessages](chatmessage.md) entre um ou mais participantes. Os participantes podem ser usuários ou aplicativos.

## <a name="methods"></a>Métodos

|  Método       |  Tipo de retorno  | Descrição| Permissões |
|:---------------|:--------|:----------|-----------|
|[Listar chats](../api/chat-list.md) | coleção [chat](chat.md) | Obter a lista de chats de que um usuário faz parte.| **Somente delegada** |
|[Obter bate-papo](../api/chat-get.md) | [chat](chat.md) | Leia as propriedades e as relações do chat.| **Somente delegada** |
|[Listar membros de chat](../api/conversationmember-list.md) | coleção [conversationMember](conversationmember.md) | Ver a lista de todos os usuários no bate-papo.| Delegado e aplicativo * |
|[Obter membro de chat](../api/conversationmember-get.md) | [conversationMember](conversationmember.md) | Obter um único usuário no bate-papo.| Delegado e aplicativo * |
|[Listar mensagens em um bate-papo](../api/chat-list-message.md)  | [chatMessage](../resources/chatmessage.md) | Receba mensagens em um bate-papo de um para um ou de grupo. | Delegado e aplicativo * |
|[Receba uma mensagem no bate-papo](../api/chat-get-message.md)  | [chatMessage](../resources/chatmessage.md) | Receba uma única mensagem em um bate-papo. | Delegado e aplicativo * |

>**Observação:** Ao usar permissões de aplicativo, certifique-se de saber como você vai obter a ID de chat. Como a lista de chats com permissões de aplicativo não é suportada, nem todos os cenários são possíveis. É possível obter IDs de chat com permissões delegadas e de notificações de [alteração para o/chats/getAllMessages](../api/subscription-post-subscriptions.md) com permissões de aplicativo.

## <a name="properties"></a>Propriedades

| Propriedade   | Tipo |Descrição|
|:---------------|:--------|:----------|
| id| String| O identificador exclusivo do chat. Somente leitura.|
| topic| String|  Opcion Assunto ou tópico do chat. Disponível apenas para bate-papos de grupo.|
| createdDateTime| dateTimeOffset|  Data e hora em que o chat foi criado. Somente leitura.|
| lastUpdatedDateTime| dateTimeOffset|  Data e hora em que o chat foi renomeado ou a associação foi alterada. lastUpdatedDateTime não é atualizado quando uma mensagem é enviada ao chat. Somente leitura.|

## <a name="relationships"></a>Relações

| Relação | Tipo |Descrição|
|:---------------|:--------|:----------|
| installedApps | Coleção [teamsAppInstallation](teamsappinstallation.md) | Uma coleção de todos os aplicativos no chat. Anulável. |
| members | coleção [conversationMember](conversationmember.md) | Uma coleção de todas as pessoas no chat. Anulável. |
| messages | [chatMessage](chatmessage.md) collection | Uma coleção de todas as mensagens no chat. Anulável. |

## <a name="json-representation"></a>Representação JSON

Veja a seguir uma representação JSON do recurso.

<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.chat"
}-->

```json
{
  "id": "string (identifier)",
  "topic": "string",
  "createdDateTime": "dateTimeOffset",
  "lastUpdatedDateTime": "dateTimeOffset"
}
```

## <a name="see-also"></a>Confira também

- [channel](channel.md)
- [chatMessage](chatmessage.md)

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "chat resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}
-->


