---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 51b72f4172933c8f4c51a3bcb544e88730b4a998
ms.sourcegitcommit: 342516a52b69fcda31442b130eb6bd7e2c8a0066
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/10/2020
ms.locfileid: "48972779"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

InputStream stream = graphClient.customRequest("/reports/getM365AppUserCounts(period='D7')/content", InputStream.class)
    .buildRequest()
    .get();

```