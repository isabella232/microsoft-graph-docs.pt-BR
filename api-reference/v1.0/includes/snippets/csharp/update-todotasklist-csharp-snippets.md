---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 10cb237494578d82547cdaaf2f6e07fc534c8538
ms.sourcegitcommit: 82da4012294b046416c9ae93d2294d80dab217f6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "48904393"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var todoTaskList = new TodoTaskList
{
    DisplayName = "Vacation Plan"
};

await graphClient.Me.Todo.Lists["AAMkADIyAAAhrbPWAAA="]
    .Request()
    .UpdateAsync(todoTaskList);

```