---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: b617e5f2335751e9c90345202daff4d20a93d67a
ms.sourcegitcommit: af4b2fc18449c33979cf6d75bd680f40602ba708
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "48603606"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var serviceConfigurationRecords = await graphClient.Domains["{domain-name}"].ServiceConfigurationRecords
    .Request()
    .GetAsync();

```