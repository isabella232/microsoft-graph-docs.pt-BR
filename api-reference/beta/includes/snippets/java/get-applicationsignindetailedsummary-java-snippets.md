---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 9d6580ab9318fc3619bdc3cff649607864d40b6a
ms.sourcegitcommit: b18f978808fef800bff9e587464a5f3e18eb7687
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/25/2019
ms.locfileid: "35856754"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

ApplicationSignInDetailedSummary applicationSignInDetailedSummary = graphClient.reports().applicationSignInDetailedSummary("'id'")
    .buildRequest()
    .get();

```