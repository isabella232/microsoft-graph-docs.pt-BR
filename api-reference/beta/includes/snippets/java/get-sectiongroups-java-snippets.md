---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: b2fc32ea3c8664846ec0f4f975effb12ce69b036
ms.sourcegitcommit: 342516a52b69fcda31442b130eb6bd7e2c8a0066
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/10/2020
ms.locfileid: "48976840"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

ISectionGroupCollectionPage sectionGroups = graphClient.me().onenote().sectionGroups("{id}").sectionGroups()
    .buildRequest()
    .get();

```