---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: eba3de6fb9dde91482ee5314776fd21517a1c1c1
ms.sourcegitcommit: b18f978808fef800bff9e587464a5f3e18eb7687
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/25/2019
ms.locfileid: "35855550"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

AdministrativeUnit administrativeUnit = new AdministrativeUnit();
administrativeUnit.displayName = "displayName-value";
administrativeUnit.description = "description-value";
administrativeUnit.visibility = "visibility-value";

graphClient.administrativeUnits("{id}")
    .buildRequest()
    .patch(administrativeUnit);

```