---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: e51288d1c3ff9472e1c8a513384245f0a71ff80f
ms.sourcegitcommit: 342516a52b69fcda31442b130eb6bd7e2c8a0066
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/10/2020
ms.locfileid: "48962238"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

graphClient.applications("{id}").tokenIssuancePolicies("{id}").reference()
    .buildRequest()
    .delete();

```