---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: f8785bc1530ed7673a7b3927243b325586506b66
ms.sourcegitcommit: c650b95ef4d0c3e93e2eb36cd6b52ed31200164f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/10/2020
ms.locfileid: "44683913"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var printerShare = new PrinterShare
{
    Name = "ShareName",
    AdditionalData = new Dictionary<string, object>()
    {
        {"printer@odata.bind", "https://graph.microsoft.com/beta/print/printers/{id}"}
    }
};

await graphClient.Print.Shares["{id}"]
    .Request()
    .UpdateAsync(printerShare);

```