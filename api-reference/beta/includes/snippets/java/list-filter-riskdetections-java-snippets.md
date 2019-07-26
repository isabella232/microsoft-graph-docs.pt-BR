---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: fea4eb16402dc8429468f6f85f3628f0c2a3d697
ms.sourcegitcommit: b18f978808fef800bff9e587464a5f3e18eb7687
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/25/2019
ms.locfileid: "35871098"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

LinkedList<Option> requestOptions = new LinkedList<Option>();
requestOptions.add(new QueryOption("$filter", "riskType eq 'unfamiliarFeatures' or riskLevel eq 'medium'"));

IRiskDetectionCollectionPage riskDetections = graphClient.riskDetections()
    .buildRequest( requestOptions )
    .get();

```