---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 4202f7b061aed8374f1a5116cd30565757b48de8
ms.sourcegitcommit: 2c8a12389b82ee5101b2bd17eae11b42e65e52c0
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "45142482"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var profileCardProperties = await graphClient.Organization["{organizationId}"].Settings.ProfileCardProperties
    .Request()
    .GetAsync();

```