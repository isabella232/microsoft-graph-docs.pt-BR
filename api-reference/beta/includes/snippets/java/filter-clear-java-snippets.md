---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: ae6e50191677b2274c31cefb56b7a13d364bb068
ms.sourcegitcommit: 342516a52b69fcda31442b130eb6bd7e2c8a0066
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/10/2020
ms.locfileid: "48965528"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

graphClient.me().drive().items("{id}").workbook().tables("{id|name}").columns("{id|name}").filter()
    .clear()
    .buildRequest()
    .post();

```