---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: a312f79942e86f8cdd57a0d08b5313c93803b034
ms.sourcegitcommit: af4b2fc18449c33979cf6d75bd680f40602ba708
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "48609348"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

await graphClient.Groups["{id}"]
    .Request()
    .DeleteAsync();

```