---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: a89c192f0bd4c1f154495f84ba1eba1b6022a161
ms.sourcegitcommit: 342516a52b69fcda31442b130eb6bd7e2c8a0066
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/10/2020
ms.locfileid: "48953414"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

IIdentityProviderAvailableProviderTypesCollectionPage availableProviderTypes = graphClient.identityProviders()
    .availableProviderTypes()
    .buildRequest()
    .get();

```