---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: eba3de6fb9dde91482ee5314776fd21517a1c1c1
ms.sourcegitcommit: 342516a52b69fcda31442b130eb6bd7e2c8a0066
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/10/2020
ms.locfileid: "48962503"
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