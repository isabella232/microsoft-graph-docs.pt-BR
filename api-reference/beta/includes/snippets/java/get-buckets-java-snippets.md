---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 442798dcebf4a3c70a471269cb1ac006ff3b0393
ms.sourcegitcommit: b18f978808fef800bff9e587464a5f3e18eb7687
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/25/2019
ms.locfileid: "35876418"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

IPlannerBucketCollectionPage buckets = graphClient.planner().plans("2txjA-BMZEq-bKi6Wfj5aGQAB1OJ").buckets()
    .buildRequest()
    .get();

```