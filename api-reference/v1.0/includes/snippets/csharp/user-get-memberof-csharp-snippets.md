---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: ec29c69ad56e51eec38dbeaa247e65bbf56f177d
ms.sourcegitcommit: 82da4012294b046416c9ae93d2294d80dab217f6
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "48905832"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var memberOf = await graphClient.Users["{id}"].MemberOf
    .Request()
    .GetAsync();

```