---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: ccb168054a6f97b9bfa1672d23e1ffd1a3414df0
ms.sourcegitcommit: b18f978808fef800bff9e587464a5f3e18eb7687
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/25/2019
ms.locfileid: "35860701"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

EducationAssignmentResource educationAssignmentResource = graphClient.education().classes("11021").assignments("19002").resources("22002")
    .buildRequest()
    .get();

```