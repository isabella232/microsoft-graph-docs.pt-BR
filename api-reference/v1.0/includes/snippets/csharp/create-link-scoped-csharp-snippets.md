---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 6877328c52532363f790466d3498068b0861188f
ms.sourcegitcommit: 5575e6607817ba23ceb0b01e2f5fc81e58bdcd1f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/22/2020
ms.locfileid: "43770978"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var type = "edit";

var scope = "organization";

await graphClient.Me.Drive.Items["{item-id}"]
    .CreateLink(type,scope,null,null,null)
    .Request()
    .PostAsync();

```