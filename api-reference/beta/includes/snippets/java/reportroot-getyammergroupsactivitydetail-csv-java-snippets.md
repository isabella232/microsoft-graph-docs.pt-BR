---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 55efc7c06a144209e055475a8de65afde42587ff
ms.sourcegitcommit: b18f978808fef800bff9e587464a5f3e18eb7687
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/25/2019
ms.locfileid: "35871295"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

IYammerGroupsActivityDetailCollectionPage getYammerGroupsActivityDetail = graphClient.reports()
    .getYammerGroupsActivityDetail('D7')
    .buildRequest()
    .get();

```