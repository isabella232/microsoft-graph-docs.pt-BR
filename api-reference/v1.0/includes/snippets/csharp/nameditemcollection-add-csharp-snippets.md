---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 65d7d2a966985f15f0d693a796986f771d9dc41f
ms.sourcegitcommit: af4b2fc18449c33979cf6d75bd680f40602ba708
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "48613195"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var name = "test7";

var formula = "=SUM(Sheet2!$A$1+Sheet2!$A$2)";

var comment = "Comment for the named item";

await graphClient.Me.Drive.Items["{id}"].Workbook.Names
    .AddFormulaLocal(name,formula,comment)
    .Request()
    .PostAsync();

```