---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 478474250ba5dcb1a8dc1c89028266220f3fb817
ms.sourcegitcommit: c4d6ccd343a6b298a2aa844f1bad66c736487251
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/11/2020
ms.locfileid: "42593538"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var homeRealmDiscoveryPolicy = await graphClient.Policies.HomeRealmDiscoveryPolicies["{id}"]
    .Request()
    .GetAsync();

```