---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: e58cd118e6558c9e8f46a9af79ab457d647d1c48
ms.sourcegitcommit: bd40e302ce04b686e86989246ab7c4cc9ad3f320
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/03/2020
ms.locfileid: "43127229"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var conditionalAccessPolicy = await graphClient.Identity.ConditionalAccess.Policies["{id}"]
    .Request()
    .GetAsync();

```