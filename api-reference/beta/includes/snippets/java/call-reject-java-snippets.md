---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 8a0d3037d98561d6776af10d5ce7c6d7a1918686
ms.sourcegitcommit: 342516a52b69fcda31442b130eb6bd7e2c8a0066
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/10/2020
ms.locfileid: "48959497"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

RejectReason reason = RejectReason.BUSY;

graphClient.communications().calls("57dab8b1-894c-409a-b240-bd8beae78896")
    .reject(reason,null)
    .buildRequest()
    .post();

```