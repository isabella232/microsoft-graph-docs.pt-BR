---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: d46d74f6682ad882bd5325847718d08f3af4abee
ms.sourcegitcommit: b18f978808fef800bff9e587464a5f3e18eb7687
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/25/2019
ms.locfileid: "35865095"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

LinkedList<Option> requestOptions = new LinkedList<Option>();
requestOptions.add(new QueryOption("startDateTime", "2017-01-01T19:00:00.0000000"));
requestOptions.add(new QueryOption("endDateTime", "2017-01-07T19:00:00.0000000"));

IEventCollectionPage calendarView = graphClient.me().calendar().calendarView()
    .buildRequest( requestOptions )
    .get();

```