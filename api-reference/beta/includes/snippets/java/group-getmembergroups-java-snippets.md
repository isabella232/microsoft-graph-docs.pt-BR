---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 42e02496d1b5bdc9085ec2cb4029be839c11897b
ms.sourcegitcommit: 342516a52b69fcda31442b130eb6bd7e2c8a0066
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/10/2020
ms.locfileid: "48965226"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

Boolean securityEnabledOnly = false;

graphClient.groups("{id}")
    .getMemberGroups(securityEnabledOnly)
    .buildRequest()
    .post();

```