---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 7139bd37faa10039e3d9a5c1c7469e60391bc666
ms.sourcegitcommit: d40d2a9266bd376d713382925323aefab285ed69
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "38751760"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var persistChanges = true;

await graphClient.Me.Drive.Items["{id}"].Workbook
    .CreateSession(persistChanges,null,null)
    .Request()
    .PostAsync();

```