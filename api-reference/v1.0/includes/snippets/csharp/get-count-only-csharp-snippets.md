---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: baabcbbdfbf03b3bdce875f29e7bb0c993496eb6
ms.sourcegitcommit: 82da4012294b046416c9ae93d2294d80dab217f6
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "48903639"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var int32 = await graphClient.Users.$count
    .Request()
    .Header("ConsistencyLevel","eventual")
    .GetAsync();

```