---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: da0ac949daf734cac5f1a82d85e5b77bd736f0a8
ms.sourcegitcommit: 4fa6b745383bb0c1864b65d612d811d64cdc079f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2019
ms.locfileid: "34479144"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var mailFolder = new MailFolder
{
    DisplayName = "displayName-value"
};

await graphClient.Me.MailFolders["{id}"]
    .Request()
    .UpdateAsync(mailFolder);

```