---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: ad887bcf9626c36fe2907e8b87c8bdf20e3c6678
ms.sourcegitcommit: 0329bbcd5f1b09a2a6c5f935a30c4560b6eed492
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2019
ms.locfileid: "36633304"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var conversationMember = await graphClient.Chats["{id}"].Members["{id}"]
    .Request()
    .GetAsync();

```