---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: bfe600ed97d4a5e9a6cd8539b1625b8a64cc5b68
ms.sourcegitcommit: 342516a52b69fcda31442b130eb6bd7e2c8a0066
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/10/2020
ms.locfileid: "48965857"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

graphClient.education().synchronizationProfiles("{id}")
    .pause()
    .buildRequest()
    .post();

```