---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 02a83cf973f851d97b5fdf579624b22926b78494
ms.sourcegitcommit: b18f978808fef800bff9e587464a5f3e18eb7687
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/25/2019
ms.locfileid: "35889063"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

IDirectoryObjectCollectionPage owners = graphClient.groups("{id}").owners()
    .buildRequest()
    .get();

```