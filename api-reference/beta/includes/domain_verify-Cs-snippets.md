---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: b1894850b69cc416e50f0c66afaae6de56989a71
ms.sourcegitcommit: 4fa6b745383bb0c1864b65d612d811d64cdc079f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2019
ms.locfileid: "34437066"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

await graphClient.Domains["contoso.com"]
    .Verify()
    .Request()
    .PostAsync();

```