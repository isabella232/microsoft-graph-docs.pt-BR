---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 17a8087759d63558be18805b25818634b25c2718
ms.sourcegitcommit: b18f978808fef800bff9e587464a5f3e18eb7687
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/25/2019
ms.locfileid: "35870966"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

IRiskyUserCollectionPage riskyUsers = graphClient.riskyUsers()
    .buildRequest()
    .get();

```