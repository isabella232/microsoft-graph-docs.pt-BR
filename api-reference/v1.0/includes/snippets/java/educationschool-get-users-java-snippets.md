---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 047a9c01fa6d2f5550fc026917e6594ca6075a41
ms.sourcegitcommit: b18f978808fef800bff9e587464a5f3e18eb7687
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/25/2019
ms.locfileid: "35887682"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

IEducationUserCollectionPage users = graphClient.education().schools("{school-id}").users()
    .buildRequest()
    .get();

```