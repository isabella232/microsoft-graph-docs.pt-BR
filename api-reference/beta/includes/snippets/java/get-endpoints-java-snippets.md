---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 5495611f7dd4d40c775c6f09bb3b63c184821296
ms.sourcegitcommit: 342516a52b69fcda31442b130eb6bd7e2c8a0066
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/10/2020
ms.locfileid: "48965087"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

ReportRoot reportRoot = graphClient.print().reports("monthlyPrintUsageSummariesByUser")
    .buildRequest()
    .get();

```