---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 254db504ef6888e54e46f75f9d9880fab4cbff18
ms.sourcegitcommit: 496410c1e256aa093eabf27f17e820d9ee91a293
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/05/2020
ms.locfileid: "46566268"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var reviewSets = await graphClient.Compliance.Ediscovery.Cases["6f65a8e4-c6a0-4cff-8a81-c9ab5df7290d"].ReviewSets
    .Request()
    .GetAsync();

```