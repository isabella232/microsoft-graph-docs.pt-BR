---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: c57e5179c583d16e2173ea463d218c3595e0dd73
ms.sourcegitcommit: 342516a52b69fcda31442b130eb6bd7e2c8a0066
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/10/2020
ms.locfileid: "48969873"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

IOutlookTaskGroupCollectionPage taskGroups = graphClient.me().outlook().taskGroups()
    .buildRequest()
    .get();

```