---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: a5263ebc64309859f70f5aaa07ff3c9d2fb44f0e
ms.sourcegitcommit: 342516a52b69fcda31442b130eb6bd7e2c8a0066
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/10/2020
ms.locfileid: "48963791"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

graphClient.me().drive().items("{item-id}")
    .buildRequest()
    .delete();

```