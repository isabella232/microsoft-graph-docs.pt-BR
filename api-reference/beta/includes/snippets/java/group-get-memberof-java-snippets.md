---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: d7c6114912c1ab89dc0ad9a897821936e75c6060
ms.sourcegitcommit: 342516a52b69fcda31442b130eb6bd7e2c8a0066
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/10/2020
ms.locfileid: "48954087"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

IDirectoryObjectCollectionWithReferencesPage memberOf = graphClient.groups("{id}").memberOf()
    .buildRequest()
    .get();

```