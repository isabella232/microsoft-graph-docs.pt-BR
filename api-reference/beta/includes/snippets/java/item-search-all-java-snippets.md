---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 1b42ee2bbf4caa19f09ed24df6fa10f9277849cb
ms.sourcegitcommit: b18f978808fef800bff9e587464a5f3e18eb7687
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/25/2019
ms.locfileid: "35860927"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

IDriveItemCollectionPage search = graphClient.me().drive()
    .search('{search-query}')
    .buildRequest()
    .get();

```