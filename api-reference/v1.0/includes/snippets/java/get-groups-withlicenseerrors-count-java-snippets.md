---
description: Automatically generated file. DO NOT MODIFY
ms.openlocfilehash: e741c2aafffdb4a2da537ec021ee6258d0e20614
ms.sourcegitcommit: 342516a52b69fcda31442b130eb6bd7e2c8a0066
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/10/2020
ms.locfileid: "48983958"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

LinkedList<Option> requestOptions = new LinkedList<Option>();
requestOptions.add(new HeaderOption("ConsistencyLevel", "eventual"));

IGroupCollectionPage groups = graphClient.groups()
    .buildRequest( requestOptions )
    .filter("hasMembersWithLicenseErrors+eq+true,")
    .select("id,displayName")
    .get();

```