---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 25ad0564c39f150301335e315afc8b4cd34144b5
ms.sourcegitcommit: 239db9e961e42b505f52de9859963a9136935f2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "46821213"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var personAnniversary = new PersonAnniversary
{
    Type = AnniversaryType.Birthday,
    Date = new Date(1980,1,8)
};

await graphClient.Me.Profile.Anniversaries
    .Request()
    .AddAsync(personAnniversary);

```