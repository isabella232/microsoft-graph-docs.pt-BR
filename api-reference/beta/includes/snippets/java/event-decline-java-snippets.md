---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: a958b4328166e105ad2b16441d545d32030d6efb
ms.sourcegitcommit: b18f978808fef800bff9e587464a5f3e18eb7687
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/25/2019
ms.locfileid: "35859727"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

String comment = "comment-value";

boolean sendResponse = True;

graphClient.me().events("{id}")
    .decline(comment,sendResponse)
    .buildRequest()
    .post();

```