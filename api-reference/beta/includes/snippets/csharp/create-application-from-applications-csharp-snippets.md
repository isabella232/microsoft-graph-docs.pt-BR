---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 187b208ac240947df0b17165815873eca3a18f51
ms.sourcegitcommit: 60dfb2ad9ef17f2918c4ee34ebb74f63e32ce2d3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/05/2019
ms.locfileid: "38000160"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var application = new Application
{
    DisplayName = "Display name"
};

await graphClient.Applications
    .Request()
    .AddAsync(application);

```