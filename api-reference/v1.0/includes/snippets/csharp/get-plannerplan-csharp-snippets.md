---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 12065c13a0c7e6ba103025ff3cd6cc28bb8c43fc
ms.sourcegitcommit: af4b2fc18449c33979cf6d75bd680f40602ba708
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "48622442"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var plannerPlan = await graphClient.Planner.Plans["{plan-id}"]
    .Request()
    .GetAsync();

```