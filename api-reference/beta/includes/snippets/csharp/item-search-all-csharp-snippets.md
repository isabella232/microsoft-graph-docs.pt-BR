---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: b4d3f8a95f745bfe542b6437b898e6f945b307a1
ms.sourcegitcommit: ef47b165f7a140cfc0309a275cb8722dd265660d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/25/2020
ms.locfileid: "46873843"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var search = await graphClient.Me.Drive
    .Search("Contoso Project")
    .Request()
    .GetAsync();

```