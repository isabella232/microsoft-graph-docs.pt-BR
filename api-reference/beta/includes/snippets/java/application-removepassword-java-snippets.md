---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 392cad2aa5870d38ba027a982d9cd1e173680efe
ms.sourcegitcommit: 342516a52b69fcda31442b130eb6bd7e2c8a0066
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/10/2020
ms.locfileid: "48961846"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

UUID keyId = UUID.fromString("f0b0b335-1d71-4883-8f98-567911bfdca6");

graphClient.applications("{id}")
    .removePassword(keyId)
    .buildRequest()
    .post();

```