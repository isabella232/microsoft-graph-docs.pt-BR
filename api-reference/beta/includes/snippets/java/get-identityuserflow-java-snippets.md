---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 098365bea1bf41db58d57e02446664fc7ff8bd8e
ms.sourcegitcommit: 342516a52b69fcda31442b130eb6bd7e2c8a0066
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/10/2020
ms.locfileid: "48953254"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

IdentityUserFlow identityUserFlow = graphClient.identity().userFlows("B2C_1_Pol1")
    .buildRequest()
    .get();

```