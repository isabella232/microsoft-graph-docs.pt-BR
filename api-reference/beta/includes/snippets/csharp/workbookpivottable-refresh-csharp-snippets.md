---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 51aa7df113adac6a19963b2e2aed4f233725dcc5
ms.sourcegitcommit: 3f7bac952864cfa67f749d902d9897f08534c0e3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/16/2019
ms.locfileid: "35716094"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

await graphClient.Drive.Root.Workbook.Worksheets["{id}"].PivotTables["{id}"]
    .Refresh()
    .Request()
    .PostAsync();

```