---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: c4be2b6c248a44d45d0f025d8e498bff5eb22884
ms.sourcegitcommit: 56c0b609dfb1bc5d900956f407d107cdab7086e8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/30/2019
ms.locfileid: "35932588"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

DriveItem driveItem = new DriveItem();
driveItem.name = "Shared legal agreements";

graphClient.drive().items("{bundle-id}")
    .buildRequest()
    .patch(driveItem);

```