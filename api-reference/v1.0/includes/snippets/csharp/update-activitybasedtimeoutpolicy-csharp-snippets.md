---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 62a1ffcf76c25cb4d1e35c46f3b721706fd52855
ms.sourcegitcommit: 5575e6607817ba23ceb0b01e2f5fc81e58bdcd1f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/22/2020
ms.locfileid: "43806257"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var activityBasedTimeoutPolicy = new ActivityBasedTimeoutPolicy
{
    Definition = new List<String>()
    {
        "definition-value"
    },
    DisplayName = "displayName-value",
    IsOrganizationDefault = true,
    Type = "type-value"
};

await graphClient.Policies.ActivityBasedTimeoutPolicies["{id}"]
    .Request()
    .UpdateAsync(activityBasedTimeoutPolicy);

```