---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: b4cb4f649e280312a2b2811675f6bca0f582b89b
ms.sourcegitcommit: b18f978808fef800bff9e587464a5f3e18eb7687
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/25/2019
ms.locfileid: "35867427"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

LinkedList<Option> requestOptions = new LinkedList<Option>();
requestOptions.add(new QueryOption("startDateTime", "2016-01-01T19:00:00.0000000"));
requestOptions.add(new QueryOption("endDateTime", "2016-10-01T19:00:00.0000000"));

IEventCollectionPage calendarView = graphClient.me().calendarView()
    .buildRequest( requestOptions )
    .get();

```