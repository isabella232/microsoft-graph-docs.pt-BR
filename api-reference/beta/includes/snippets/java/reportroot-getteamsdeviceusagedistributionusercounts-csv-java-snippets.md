---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 34097233a446ada7386fdffaa20ca5d7f4cd36c9
ms.sourcegitcommit: b18f978808fef800bff9e587464a5f3e18eb7687
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/25/2019
ms.locfileid: "35871836"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

ITeamsDeviceUsageDistributionUserCountsCollectionPage getTeamsDeviceUsageDistributionUserCounts = graphClient.reports()
    .getTeamsDeviceUsageDistributionUserCounts('D7')
    .buildRequest()
    .get();

```