---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 9647332c813fa12b69fc3e4b86a9ce44bdffc2d5
ms.sourcegitcommit: 342516a52b69fcda31442b130eb6bd7e2c8a0066
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/10/2020
ms.locfileid: "48958559"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

WorkbookChartLineFormat workbookChartLineFormat = graphClient.me().drive().items("{id}").workbook().worksheets("{id|name}").charts("{name}").axes().seriesAxis().format().line()
    .buildRequest()
    .get();

```