---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 354d346e6f02503cb3425f85f49e181eb0e51a84
ms.sourcegitcommit: 1ec5a7be90790aaebdf6d85d93ab0c72b381c9c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/24/2020
ms.locfileid: "44862558"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var me = await graphClient.Me
    .Request()
    .Select("MailboxSettings")
    .GetAsync();

var userPurpose = me.MailboxSettings.UserPurpose;

```