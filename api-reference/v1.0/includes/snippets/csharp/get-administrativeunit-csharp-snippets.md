---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: c16dce93d5645f81598abf4b90440950f455043f
ms.sourcegitcommit: a3fc420a5639c0f4e89af2b602db17392e176802
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/23/2020
ms.locfileid: "48223461"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var administrativeUnit = await graphClient.Directory.AdministrativeUnits["{id}"]
    .Request()
    .GetAsync();

```