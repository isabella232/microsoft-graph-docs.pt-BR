---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 432f6a04bbf490df9d0576750aee0464dcc1f2f7
ms.sourcegitcommit: b18f978808fef800bff9e587464a5f3e18eb7687
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/25/2019
ms.locfileid: "35883524"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

graphClient.devices("{id}")
    .buildRequest()
    .delete();

```