---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 65747b9ba4297db74499519b13bfe5a14ea33c59
ms.sourcegitcommit: 60dfb2ad9ef17f2918c4ee34ebb74f63e32ce2d3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/05/2019
ms.locfileid: "37995558"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

await graphClient.Applications["{id}"].ExtensionProperties["{id}"]
    .Request()
    .DeleteAsync();

```