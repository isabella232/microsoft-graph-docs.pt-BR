---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: fe810941914ea593b659f5c0e147daa846b29811
ms.sourcegitcommit: b18f978808fef800bff9e587464a5f3e18eb7687
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/25/2019
ms.locfileid: "35864419"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

ChatMessage chatMessage = new ChatMessage();
ItemBody body = new ItemBody();
body.contentType = BodyType.HTML;
body.content = "Hello World";
chatMessage.body = body;

graphClient.teams("{id}").channels("{id}").messages("{id}").replies()
    .buildRequest()
    .post(chatMessage);

```