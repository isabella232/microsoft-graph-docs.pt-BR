---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 7582ffcff09ca12f7301d8e2ca47f0b86028765a
ms.sourcegitcommit: b18f978808fef800bff9e587464a5f3e18eb7687
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/25/2019
ms.locfileid: "35862299"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

graphClient.directoryroles("{id}").members("{id}").reference()
    .buildRequest()
    .delete();

```