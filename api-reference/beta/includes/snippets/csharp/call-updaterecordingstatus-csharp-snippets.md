---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 2a0d02e2ff63f785db2fb981a128505540e20a6a
ms.sourcegitcommit: f27e81daeff242e623d1a3627405667310395734
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/25/2019
ms.locfileid: "39843829"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var clientContext = "clientContext-value";

var status = RecordingStatus.NotRecording | RecordingStatus.Recording | RecordingStatus.Failed;

await graphClient.Communications.Calls["{id}"]
    .UpdateRecordingStatus(status,clientContext)
    .Request()
    .PostAsync();

```