---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 99adde1d8b75759bbb13edf596ba67eaa6a48546
ms.sourcegitcommit: b18f978808fef800bff9e587464a5f3e18eb7687
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/25/2019
ms.locfileid: "35870964"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

LinkedList<Option> requestOptions = new LinkedList<Option>();
requestOptions.add(new QueryOption("$filter", "riskLevel eq microsoft.graph.riskLevel'medium'"));

IRiskyUserCollectionPage riskyUsers = graphClient.riskyUsers()
    .buildRequest( requestOptions )
    .get();

```