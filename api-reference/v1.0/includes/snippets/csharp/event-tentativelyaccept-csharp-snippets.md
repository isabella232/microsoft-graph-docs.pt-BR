---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 00c77b252745818d17f66249dc506eaaf48359b7
ms.sourcegitcommit: 5a1373f2ccd9ee813fc60d42e7ac6b115b5f9f66
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/21/2020
ms.locfileid: "44338855"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var comment = "comment-value";

var sendResponse = true;

await graphClient.Me.Events["{id}"]
    .TentativelyAccept(null,sendResponse,comment)
    .Request()
    .PostAsync();

```