---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 33f5973c4041b5a0a2bf267167e7dff6032318be
ms.sourcegitcommit: 94c8985a3956622ea90f7e641f894d57b0982eb9
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/02/2020
ms.locfileid: "44215903"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

String message = "message-value";

graphClient.teams("{teamId}").schedule().timeOffRequests("{timeOffRequestId}")
    .decline(message)
    .buildRequest()
    .post();

```