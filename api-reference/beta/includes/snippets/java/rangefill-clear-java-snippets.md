---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 87cf60998b21167cfce42edea047226c8102895f
ms.sourcegitcommit: 342516a52b69fcda31442b130eb6bd7e2c8a0066
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/10/2020
ms.locfileid: "48976244"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

graphClient.me().drive().items("{id}").workbook().names("{name}")
    .range().format().fill()
    .clear()
    .buildRequest()
    .post();

```