---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 918d92298cf5ceaa5b01bda29b96e2da4a101fe3
ms.sourcegitcommit: 342516a52b69fcda31442b130eb6bd7e2c8a0066
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/10/2020
ms.locfileid: "48968607"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

IPasswordlessMicrosoftAuthenticatorAuthenticationMethodCollectionPage passwordlessMicrosoftAuthenticatorMethods = graphClient.me().authentication().passwordlessMicrosoftAuthenticatorMethods()
    .buildRequest()
    .get();

```