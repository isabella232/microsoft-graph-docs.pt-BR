---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: ca3ef066a958b34273c989dc025b861c22840472
ms.sourcegitcommit: 62507617292d5ad8598e83a8a253c986d9bac787
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2019
ms.locfileid: "37936675"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var namedLocations = await graphClient.ConditionalAccess.NamedLocations
    .Request()
    .Filter("microsoft.graph.countryNamedLocation/countriesAndRegions/any(c: c eq 'CA')")
    .GetAsync();

```