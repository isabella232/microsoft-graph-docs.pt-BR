---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 995a4b1e3d28de884c8b35db0d2eb5615ac8a8e8
ms.sourcegitcommit: 342516a52b69fcda31442b130eb6bd7e2c8a0066
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/10/2020
ms.locfileid: "48972128"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

LinkedList<String> groupIdsList = new LinkedList<String>();
groupIdsList.add("groupIds-value");

graphClient.contacts("{id}")
    .checkMemberGroups(groupIdsList)
    .buildRequest()
    .post();

```