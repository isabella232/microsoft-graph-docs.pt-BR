---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 0dff7524a01d93d325ab604907a2f92f0f19f95d
ms.sourcegitcommit: b18f978808fef800bff9e587464a5f3e18eb7687
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/25/2019
ms.locfileid: "35872681"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

ISharePointSiteUsageDetailCollectionPage getSharePointSiteUsageDetail = graphClient.reports()
    .getSharePointSiteUsageDetail('D7')
    .buildRequest()
    .get();

```