---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: cf9d21794a826b5f0a4afa64a51131f5be466af2
ms.sourcegitcommit: 342516a52b69fcda31442b130eb6bd7e2c8a0066
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/10/2020
ms.locfileid: "48977517"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

WorkbookApplication workbookApplication = graphClient.me().drive().items("{id}").workbook().application()
    .buildRequest()
    .get();

```