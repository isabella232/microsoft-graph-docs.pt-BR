---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 4629e70a9f8a9d220b6f033ac03566a33c437063
ms.sourcegitcommit: c75356177c73ec480cec868a4404a63dca5b078d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/15/2020
ms.locfileid: "43512303"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var list = await graphClient.Sites["{site-id}"].Lists["{list-title}"]
    .Request()
    .GetAsync();

```