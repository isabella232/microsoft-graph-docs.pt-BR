---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 2fa54a5ec44a0080798b3437366c66037af56234
ms.sourcegitcommit: 342516a52b69fcda31442b130eb6bd7e2c8a0066
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/10/2020
ms.locfileid: "48982033"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

byte[] stream = Base64.getDecoder().decode("The contents of the file goes here.");
    graphClient.me().drive().items("{item-id}")
    .buildRequest()
    .put(stream);

```