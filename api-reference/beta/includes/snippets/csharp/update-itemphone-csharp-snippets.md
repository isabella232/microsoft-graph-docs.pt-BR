---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 4e7757719e959b8e9c8ef8e6174941d8e9a8840c
ms.sourcegitcommit: 60dfb2ad9ef17f2918c4ee34ebb74f63e32ce2d3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/05/2019
ms.locfileid: "37997319"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var itemPhone = new ItemPhone
{
    DisplayName = "displayName-value",
    Type = PhoneType.Home,
    Number = "number-value"
};

await graphClient.Me.Profile.Phones["{id}"]
    .Request()
    .UpdateAsync(itemPhone);

```