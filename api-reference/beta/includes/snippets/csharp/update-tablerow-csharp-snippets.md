---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 64fd80e19e377e51123ac066f4369960e4246cc6
ms.sourcegitcommit: af4b2fc18449c33979cf6d75bd680f40602ba708
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "48616568"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var workbookTableRow = new WorkbookTableRow
{
    Index = 99,
    Values = "values-value"
};

await graphClient.Me.Drive.Items["{id}"].Workbook.Tables["{id|name}"].Rows["{index}"]
    .Request()
    .UpdateAsync(workbookTableRow);

```