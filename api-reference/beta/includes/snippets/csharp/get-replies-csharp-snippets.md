---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: ca7244c033b2e0fc40840b036cf6e1b53e52f17c
ms.sourcegitcommit: d8a58221ed1f2b7b7073fd621da4737e11ba53c5
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/11/2019
ms.locfileid: "36838859"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var replies = await graphClient.Drive.Root.Workbook.Comments["{id}"].Replies
    .Request()
    .GetAsync();

```