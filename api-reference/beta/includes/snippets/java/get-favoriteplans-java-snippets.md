---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 79627c39db6c9725e15cfd4f3db7aaff1c67b43e
ms.sourcegitcommit: b18f978808fef800bff9e587464a5f3e18eb7687
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/25/2019
ms.locfileid: "35876180"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

IPlannerPlanCollectionPage favoritePlans = graphClient.me().planner().favoritePlans()
    .buildRequest()
    .get();

```