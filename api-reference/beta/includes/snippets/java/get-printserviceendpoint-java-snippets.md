---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 9531b3e06dc313714251e75ad7ae5a3fe360ab5a
ms.sourcegitcommit: 342516a52b69fcda31442b130eb6bd7e2c8a0066
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/10/2020
ms.locfileid: "48968191"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

PrintServiceEndpoint printServiceEndpoint = graphClient.print().services("{id}").endpoints("{name}")
    .buildRequest()
    .get();

```