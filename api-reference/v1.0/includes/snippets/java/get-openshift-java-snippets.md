---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: d5e950f7d7a322e3b918be4c3cfadcb7573caf8b
ms.sourcegitcommit: d4114bac58628527611e83e436132c6581a19c52
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/13/2020
ms.locfileid: "44216575"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

IOpenShiftCollectionPage openShifts = graphClient.teams("{id}").schedule().openShifts()
    .buildRequest()
    .get();

```