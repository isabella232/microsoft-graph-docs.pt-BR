---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: d0e0e58482e0b16ac061e2bf429caa55b1088ff9
ms.sourcegitcommit: d8a425766aa6a56027b8576bbec6a9d1ae3e079c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/21/2019
ms.locfileid: "37544132"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

ConversationThread conversationThread = new ConversationThread();
conversationThread.isLocked = true;

graphClient.groups("{id}").threads("{id}")
    .buildRequest()
    .patch(conversationThread);

```