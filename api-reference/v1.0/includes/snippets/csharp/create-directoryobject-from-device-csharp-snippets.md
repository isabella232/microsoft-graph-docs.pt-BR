---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: d225f7453a1ad24e87d0d48a85be432447565ff8
ms.sourcegitcommit: 0545b031585e605dc3a0fde481015f51f79819c4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/22/2020
ms.locfileid: "45224541"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var directoryObject = new DirectoryObject
{
    Id = "{id}"
};

await graphClient.Devices["{id}"].RegisteredUsers.References
    .Request()
    .AddAsync(directoryObject);

```