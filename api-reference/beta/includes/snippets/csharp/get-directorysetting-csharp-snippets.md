---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: d23dc968d33e2279a2ec6f270756ca6a96738296
ms.sourcegitcommit: af4b2fc18449c33979cf6d75bd680f40602ba708
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "48610276"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var directorySetting = await graphClient.Settings["{id}"]
    .Request()
    .GetAsync();

```