---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 0a1e9f3f118db62f7e026705431641bf54aed557
ms.sourcegitcommit: c20276369a8834a259f24038e7ee5c33de02660b
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/07/2020
ms.locfileid: "48375718"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var group = await graphClient.Groups["{id}"].MemberOf
    .Request()
    .Header("ConsistencyLevel","eventual")
    .Search("displayName:Video")
    .OrderBy("displayName ")
    .GetAsync();

```