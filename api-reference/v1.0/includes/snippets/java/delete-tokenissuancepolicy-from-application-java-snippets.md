---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: e51288d1c3ff9472e1c8a513384245f0a71ff80f
ms.sourcegitcommit: 5575e6607817ba23ceb0b01e2f5fc81e58bdcd1f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/22/2020
ms.locfileid: "43806697"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

graphClient.applications("{id}").tokenIssuancePolicies("{id}").reference()
    .buildRequest()
    .delete();

```