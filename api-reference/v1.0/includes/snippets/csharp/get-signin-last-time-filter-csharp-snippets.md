---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 7be05ffd1451446b5ecb56e921b4bf49e81f0f18
ms.sourcegitcommit: 82da4012294b046416c9ae93d2294d80dab217f6
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "48905670"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var users = await graphClient.Users
    .Request()
    .Filter("startswith(displayName,'Eric'),")
    .Select("displayName,signInActivity")
    .GetAsync();

```