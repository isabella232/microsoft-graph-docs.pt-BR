---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 3fc0292af888b474ad640d4625f7ffa96455fcba
ms.sourcegitcommit: b18f978808fef800bff9e587464a5f3e18eb7687
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/25/2019
ms.locfileid: "35877083"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

Participant Participant = graphClient.app().calls("{id}").participants("{id}")
    .buildRequest()
    .get();

```