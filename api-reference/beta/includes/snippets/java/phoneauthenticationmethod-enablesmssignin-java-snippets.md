---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 569519d05c3964c9f29236669f34f7631fbbdf5a
ms.sourcegitcommit: 342516a52b69fcda31442b130eb6bd7e2c8a0066
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/10/2020
ms.locfileid: "48971183"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

graphClient.me().authentication().phoneMethods("3179e48a-750b-4051-897c-87b9720928f7")
    .enableSmsSignIn()
    .buildRequest()
    .post();

```