---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 1112194460147ae08c5ae03fc3cbe6468fe0ced7
ms.sourcegitcommit: b18f978808fef800bff9e587464a5f3e18eb7687
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/25/2019
ms.locfileid: "35855943"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

graphClient.accessReviews("2975E9B5-44CE-4E71-93D3-30F03B5AA992")
    .sendReminder()
    .buildRequest()
    .post();

```