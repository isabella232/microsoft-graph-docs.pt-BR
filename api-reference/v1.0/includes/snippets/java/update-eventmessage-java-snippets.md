---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: cb512d8a538be0125f344cea168bfec398fc3ef0
ms.sourcegitcommit: 82da4012294b046416c9ae93d2294d80dab217f6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "48907325"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

Message message = new Message();
message.isRead = true;

graphClient.me().messages("{id}")
    .buildRequest()
    .patch(message);

```