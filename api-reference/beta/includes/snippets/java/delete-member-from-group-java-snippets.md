---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: cb6b92ba3bf367bfbb60a62df73efbc04910c9d0
ms.sourcegitcommit: 342516a52b69fcda31442b130eb6bd7e2c8a0066
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/10/2020
ms.locfileid: "48954225"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

graphClient.groups("{group-id}").members("{directory-object-id}").reference()
    .buildRequest()
    .delete();

```