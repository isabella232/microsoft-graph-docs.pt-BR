---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 85a48c2ec69446cf6083cc569e2ac6f60bbd9db3
ms.sourcegitcommit: a3fc420a5639c0f4e89af2b602db17392e176802
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/23/2020
ms.locfileid: "48223287"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

await graphClient.Directory.AdministrativeUnits["{id}"]
    .Request()
    .DeleteAsync();

```