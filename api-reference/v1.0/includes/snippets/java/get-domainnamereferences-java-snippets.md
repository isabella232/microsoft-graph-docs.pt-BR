---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 54e8f398ac3a31b1906ec577380c73aa2e999908
ms.sourcegitcommit: 342516a52b69fcda31442b130eb6bd7e2c8a0066
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/10/2020
ms.locfileid: "48983350"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

IDirectoryObjectCollectionWithReferencesPage domainNameReferences = graphClient.domains("{domain-name}").domainNameReferences()
    .buildRequest()
    .get();

```