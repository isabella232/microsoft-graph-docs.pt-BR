---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 472c2473e9f09a93b5e703e010c7528492e64069
ms.sourcegitcommit: 342516a52b69fcda31442b130eb6bd7e2c8a0066
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/10/2020
ms.locfileid: "48960862"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

IBookingAppointmentCollectionPage appointments = graphClient.bookingBusinesses("Contosolunchdelivery@M365B489948.onmicrosoft.com").appointments()
    .buildRequest()
    .get();

```