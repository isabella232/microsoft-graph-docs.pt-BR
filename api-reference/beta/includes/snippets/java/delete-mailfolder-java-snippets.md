---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 11888dc38350d4272d7ecf6ef2a025fa3a303cb0
ms.sourcegitcommit: 342516a52b69fcda31442b130eb6bd7e2c8a0066
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/10/2020
ms.locfileid: "48977441"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

graphClient.me().mailFolders("AAMkAGVmMDEzM")
    .buildRequest()
    .delete();

```