---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: ac582e24a67592421f38de2d454f521e0960e08a
ms.sourcegitcommit: c650b95ef4d0c3e93e2eb36cd6b52ed31200164f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/10/2020
ms.locfileid: "44684928"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var conversationThread = new ConversationThread
{
    Topic = "topic-value",
    Posts = (IConversationThreadPostsCollectionPage)new List<Post>()
    {
        new Post
        {
            Body = new ItemBody
            {
                ContentType = BodyType.Html,
                Content = "this is body content"
            }
        }
    }
};

await graphClient.Groups["{id}"].Conversations["{id}"].Threads
    .Request()
    .AddAsync(conversationThread);

```