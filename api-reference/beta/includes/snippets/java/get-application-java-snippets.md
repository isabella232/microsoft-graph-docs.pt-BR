---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 511df171efbcf38cd542e8d7a27a29c2fc5c66a2
ms.sourcegitcommit: 342516a52b69fcda31442b130eb6bd7e2c8a0066
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/10/2020
ms.locfileid: "48962154"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

Application application = graphClient.applications("{id}")
    .buildRequest()
    .get();

```