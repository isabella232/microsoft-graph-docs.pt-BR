---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 1267e49f7033be43f48137a446421da815685d8b
ms.sourcegitcommit: b18f978808fef800bff9e587464a5f3e18eb7687
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/25/2019
ms.locfileid: "35882061"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

WorkbookChartAxis workbookChartAxis = graphClient.me().drive().items("{id}").workbook().worksheets("{id|name}").charts("{name}").axes().valueAxis()
    .buildRequest()
    .get();

```