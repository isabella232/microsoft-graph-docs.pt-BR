---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 68e747bf9da42fd85bad534b58ee60c91437c164
ms.sourcegitcommit: b18f978808fef800bff9e587464a5f3e18eb7687
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/25/2019
ms.locfileid: "35857231"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

String applyTo = "applyTo-value";

graphClient.me().drive().items("{id}").workbook().names("{name}")
    .range()
    .clear(applyTo)
    .buildRequest()
    .post();

```