---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 95167279ef78186114d249037bebd96ba34dd882
ms.sourcegitcommit: d40d2a9266bd376d713382925323aefab285ed69
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "38747869"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var id = "5793aa3b-cca9-4794-679a240f8b58";

await graphClient.ServicePrincipals["{id}"]
    .DeletePasswordSingleSignOnCredentials(id)
    .Request()
    .PostAsync();

```