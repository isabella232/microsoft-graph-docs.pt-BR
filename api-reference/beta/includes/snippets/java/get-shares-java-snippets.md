---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: a2c05ad8c2ef657b254f2aebed1fc6ad0994298c
ms.sourcegitcommit: 342516a52b69fcda31442b130eb6bd7e2c8a0066
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/10/2020
ms.locfileid: "48967054"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

IPrinterShareCollectionPage shares = graphClient.print().shares()
    .buildRequest()
    .get();

```