---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: a848619eabdc27cdfc95b0f93a890affd9b3c2ea
ms.sourcegitcommit: b18f978808fef800bff9e587464a5f3e18eb7687
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/25/2019
ms.locfileid: "35891827"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

Report report = graphClient.reports()
    .getEmailActivityCounts('D7')
    .buildRequest()
    .get();

```