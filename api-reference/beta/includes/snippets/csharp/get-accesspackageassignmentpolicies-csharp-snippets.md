---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 3429370eed26011f96970b7504ed53f49bda2a8e
ms.sourcegitcommit: f27e81daeff242e623d1a3627405667310395734
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/25/2019
ms.locfileid: "37992825"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var accessPackageAssignmentPolicies = await graphClient.IdentityGovernance.EntitlementManagement.AccessPackageAssignmentPolicies
    .Request()
    .GetAsync();

```