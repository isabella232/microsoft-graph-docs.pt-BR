---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 0779b6208ff720db4d7cfd6738650fb2a3d7856d
ms.sourcegitcommit: b18f978808fef800bff9e587464a5f3e18eb7687
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/25/2019
ms.locfileid: "35887221"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

Message message = graphClient.me().messages("AAMkADYAAAImV_jAAA=")
    .buildRequest()
    .expand("eventMessage/event")
    .get();

```