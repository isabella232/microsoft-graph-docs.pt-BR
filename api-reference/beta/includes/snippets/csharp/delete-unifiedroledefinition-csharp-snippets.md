---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 6aef5a3a699ae194087a96859c99f983263e03fe
ms.sourcegitcommit: f50b1feff72182d1e19bfa346304beaf29558b68
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2019
ms.locfileid: "36461577"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

await graphClient.RoleManagement.Directory.RoleDefinitions["f189965f-f560-4c59-9101-933d4c87a91a"]
    .Request()
    .DeleteAsync();

```