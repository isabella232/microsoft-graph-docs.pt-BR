---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 01666af7421c98ce8a75e3026f6ea8217b599f35
ms.sourcegitcommit: 342516a52b69fcda31442b130eb6bd7e2c8a0066
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/10/2020
ms.locfileid: "48963876"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

String type = "embed";

graphClient.me().drive().items("{item-id}")
    .createLink(type,null,null,null,null,null)
    .buildRequest()
    .post();

```