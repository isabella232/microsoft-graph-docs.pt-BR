---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: de8df7c2ce5d4d69bcd2e8eeb8edba6344ef3adb
ms.sourcegitcommit: b18f978808fef800bff9e587464a5f3e18eb7687
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/25/2019
ms.locfileid: "35880898"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

IdentityProvider identityProvider = new IdentityProvider();
identityProvider.clientSecret = "1111111111111";

graphClient.identityProviders("Amazon-OAuth")
    .buildRequest()
    .patch(identityProvider);

```