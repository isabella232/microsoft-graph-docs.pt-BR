---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 240b686fd23e8a215156c3e5d3a9c94b429cb4cc
ms.sourcegitcommit: 342516a52b69fcda31442b130eb6bd7e2c8a0066
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/10/2020
ms.locfileid: "48971070"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

Schedule schedule = new Schedule();
schedule.enabled = true;
schedule.timeZone = "America/Chicago";

graphClient.teams("{teamId}").schedule()
    .buildRequest()
    .put(schedule);

```