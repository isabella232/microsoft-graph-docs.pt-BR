---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 43c63a9b10f7e1c08d25dd68241af07a30d20930
ms.sourcegitcommit: 5a1373f2ccd9ee813fc60d42e7ac6b115b5f9f66
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/21/2020
ms.locfileid: "44334369"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var groupIds = new List<String>()
{
    "groupIds-value"
};

await graphClient.ServicePrincipals["{id}"]
    .CheckMemberGroups(groupIds)
    .Request()
    .PostAsync();

```