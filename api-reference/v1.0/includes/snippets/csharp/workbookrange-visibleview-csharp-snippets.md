---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: a3c77da0340d6c872bc11f9e95b243fbf043b9d6
ms.sourcegitcommit: b18f978808fef800bff9e587464a5f3e18eb7687
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/25/2019
ms.locfileid: "35884869"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var workbookRangeView = await graphClient.Me.Drive.Root.Workbook.Worksheets["{id}"]
    .Range('A1:Z10')
    .VisibleView()
    .Request()
    .GetAsync();

```