---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: e2d2facaa34f9b7504de4e282609b11fbf97f4fd
ms.sourcegitcommit: 94c8985a3956622ea90f7e641f894d57b0982eb9
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/02/2020
ms.locfileid: "44218194"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

String message = "message-value";

graphClient.teams("{teamId}").schedule().swapShiftsChangeRequests("{swapShiftChangeRequestId}")
    .approve(message)
    .buildRequest()
    .post();

```