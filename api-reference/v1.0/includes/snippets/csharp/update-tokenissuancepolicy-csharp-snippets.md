---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: ac98cafae299c7399c2744d4ad60cdd6a6def3d4
ms.sourcegitcommit: 5575e6607817ba23ceb0b01e2f5fc81e58bdcd1f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/22/2020
ms.locfileid: "43719449"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var tokenIssuancePolicy = new TokenIssuancePolicy
{
    Definition = new List<String>()
    {
        "definition-value"
    },
    DisplayName = "displayName-value",
    IsOrganizationDefault = true,
    Type = "type-value"
};

await graphClient.Policies.TokenIssuancePolicies["{id}"]
    .Request()
    .UpdateAsync(tokenIssuancePolicy);

```