---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: a891fbc5807ebc35d07056057f7b62eda7ced0fe
ms.sourcegitcommit: 5a1373f2ccd9ee813fc60d42e7ac6b115b5f9f66
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/21/2020
ms.locfileid: "44335928"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var memberOf = await graphClient.ServicePrincipals["{id}"].MemberOf
    .Request()
    .GetAsync();

```