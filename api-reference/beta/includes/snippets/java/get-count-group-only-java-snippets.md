---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 2bf53f83dda9e4b2c0929209ab482943532406f8
ms.sourcegitcommit: 342516a52b69fcda31442b130eb6bd7e2c8a0066
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/10/2020
ms.locfileid: "48954098"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

LinkedList<Option> requestOptions = new LinkedList<Option>();
requestOptions.add(new HeaderOption("ConsistencyLevel", "eventual"));

int int32 = graphClient.servicePrincipals("{id}").memberOf().microsoft.graph.group().count()
    .buildRequest( requestOptions )
    .get();

```