---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 56c96356249c3e9f4a0e80f7c27b7e932d7719c9
ms.sourcegitcommit: b18f978808fef800bff9e587464a5f3e18eb7687
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/25/2019
ms.locfileid: "35893871"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

Report report = graphClient.reports()
    .getYammerGroupsActivityDetail('D7')
    .buildRequest()
    .get();

```