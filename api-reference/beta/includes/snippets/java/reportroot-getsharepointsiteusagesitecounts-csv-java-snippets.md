---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 46a5e60e4821a6bcc130ed9c31782b65e87633f3
ms.sourcegitcommit: b18f978808fef800bff9e587464a5f3e18eb7687
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/25/2019
ms.locfileid: "35872595"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

ISharePointSiteUsageSiteCountsCollectionPage getSharePointSiteUsageSiteCounts = graphClient.reports()
    .getSharePointSiteUsageSiteCounts('D7')
    .buildRequest()
    .get();

```