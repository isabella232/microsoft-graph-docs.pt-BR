---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 867b75745141fc4b570f35b3e8703301af39863a
ms.sourcegitcommit: b18f978808fef800bff9e587464a5f3e18eb7687
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/25/2019
ms.locfileid: "35875781"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

graphClient.privilegedRoles("{id}")
    .selfDeactivate()
    .buildRequest()
    .post();

```