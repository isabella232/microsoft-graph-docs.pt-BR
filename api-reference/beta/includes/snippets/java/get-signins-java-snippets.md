---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 09e3f446180637d300e1996204a69c2d1df1b15f
ms.sourcegitcommit: b18f978808fef800bff9e587464a5f3e18eb7687
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/25/2019
ms.locfileid: "35869740"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

ISignInCollectionPage signIns = graphClient.auditLogs().signIns()
    .buildRequest()
    .get();

```