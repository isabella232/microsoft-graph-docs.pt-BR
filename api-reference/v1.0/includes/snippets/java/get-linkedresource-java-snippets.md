---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 07c790c74f7d16f519d300cbf30007aca4e6c67e
ms.sourcegitcommit: 82da4012294b046416c9ae93d2294d80dab217f6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "48903432"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

ILinkedResourceCollectionPage linkedResources = graphClient.me().todo().lists("dfsdc-f9dfdfs-dcsda9").tasks("e2dc-f9cce2-dce29").linkedResources()
    .buildRequest()
    .get();

```