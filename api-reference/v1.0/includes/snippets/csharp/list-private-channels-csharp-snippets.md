---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 4178a1c7cce23bca0862d0de29f98c62bd9a8a79
ms.sourcegitcommit: c20276369a8834a259f24038e7ee5c33de02660b
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/07/2020
ms.locfileid: "48373593"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var channels = await graphClient.Teams["{id}"].Channels
    .Request()
    .Filter("membershipType eq 'private'")
    .GetAsync();

```