---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 29b005c7017867e97757316602bf98d0a11dcb4f
ms.sourcegitcommit: 46ee19b244349e2a1537f0c44c576d7c01cf03a9
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/05/2019
ms.locfileid: "37402519"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var id = "id-value";

var groupId = "groupId-value";

await graphClient.Me.Onenote.Pages["{id}"]
    .CopyToSection(id,groupId,null,null)
    .Request()
    .PostAsync();

```