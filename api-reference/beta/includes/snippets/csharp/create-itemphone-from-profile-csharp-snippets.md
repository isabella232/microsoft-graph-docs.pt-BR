---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: e5886dab6601644633598b35abc3ab83d4d89b67
ms.sourcegitcommit: 60dfb2ad9ef17f2918c4ee34ebb74f63e32ce2d3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/05/2019
ms.locfileid: "37996520"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var itemPhone = new ItemPhone
{
    DisplayName = "displayName-value",
    Type = PhoneType.Home,
    Number = "number-value"
};

await graphClient.Me.Profile.Phones
    .Request()
    .AddAsync(itemPhone);

```