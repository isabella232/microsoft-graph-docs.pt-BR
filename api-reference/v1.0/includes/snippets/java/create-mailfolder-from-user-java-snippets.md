---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 913a7f648ab7dcb1d5cd376493dd421f783da703
ms.sourcegitcommit: b18f978808fef800bff9e587464a5f3e18eb7687
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/25/2019
ms.locfileid: "35885659"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

MailFolder mailFolder = new MailFolder();
mailFolder.displayName = "displayName-value";

graphClient.me().mailFolders()
    .buildRequest()
    .post(mailFolder);

```