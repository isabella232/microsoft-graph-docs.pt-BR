---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: fb5c5ab7c30e65d90e62f5f47a1cb64792179b78
ms.sourcegitcommit: b18f978808fef800bff9e587464a5f3e18eb7687
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/25/2019
ms.locfileid: "35888955"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var workbookRange = await graphClient.Me.Drive.Items["{id}"].Workbook.Names["{name}"]
    .Range()
    .LastColumn()
    .Request()
    .GetAsync();

```