---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: c39b81565f0fb560900a4f51426eb996e3d71eb1
ms.sourcegitcommit: 94c8985a3956622ea90f7e641f894d57b0982eb9
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/02/2020
ms.locfileid: "44217105"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var message = "message-value";

await graphClient.Teams["{teamId}"].Schedule.TimeOffRequests["{timeOffRequestId}"]
    .Decline(message)
    .Request()
    .PostAsync();

```