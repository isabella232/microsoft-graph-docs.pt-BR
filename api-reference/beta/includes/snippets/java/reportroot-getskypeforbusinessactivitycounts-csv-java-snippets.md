---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 9c4cbc6e794e1bcef17143dd19bbc666c64f61c4
ms.sourcegitcommit: b18f978808fef800bff9e587464a5f3e18eb7687
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/25/2019
ms.locfileid: "35872428"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

ISkypeForBusinessActivityCountsCollectionPage getSkypeForBusinessActivityCounts = graphClient.reports()
    .getSkypeForBusinessActivityCounts('D7')
    .buildRequest()
    .get();

```