---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: fb63360d8e861bd04b95e542367ce92001f7ee32
ms.sourcegitcommit: af4b2fc18449c33979cf6d75bd680f40602ba708
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "48612224"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var workbookTable = new WorkbookTable
{
    Name = "name-value",
    ShowHeaders = true,
    ShowTotals = true,
    Style = "style-value"
};

await graphClient.Me.Drive.Items["{id}"].Workbook.Tables["{id|name}"]
    .Request()
    .UpdateAsync(workbookTable);

```