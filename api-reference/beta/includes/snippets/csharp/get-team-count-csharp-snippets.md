---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: be5f88ecdfdca069ce3f1a88ee43de429e95009e
ms.sourcegitcommit: 5a1373f2ccd9ee813fc60d42e7ac6b115b5f9f66
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/21/2020
ms.locfileid: "44334738"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var servicePrincipals = await graphClient.ServicePrincipals
    .Request()
    .Header("ConsistencyLevel","eventual")
    .Search("displayName:Team")
    .GetAsync();

```