---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: a6cb271e6a44a8942b313a85e4bf60e7664ed2cb
ms.sourcegitcommit: 7b286637aa332cfd534a41526950b4f6272e0fd7
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/05/2020
ms.locfileid: "41774772"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var calendar = await graphClient.Users["meganb@contoso.OnMicrosoft.com"].Calendars["AAMkADlAABhbftjAAA="]
    .Request()
    .GetAsync();

```