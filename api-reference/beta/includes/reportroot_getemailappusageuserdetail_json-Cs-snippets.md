---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 73cfc36775de434ec6596e60e8157dae4b602680
ms.sourcegitcommit: 4fa6b745383bb0c1864b65d612d811d64cdc079f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2019
ms.locfileid: "34442127"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var getEmailAppUsageUserDetail = await graphClient.Reports.GetEmailAppUsageUserDetail('D7')
    .Request()
    .GetAsync();

```