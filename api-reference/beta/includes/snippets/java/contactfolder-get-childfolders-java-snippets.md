---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 7902d05724ec6a8924047ed39849e8896f326588
ms.sourcegitcommit: 342516a52b69fcda31442b130eb6bd7e2c8a0066
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/10/2020
ms.locfileid: "48957080"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

IContactFolderCollectionPage childFolders = graphClient.me().contactFolders("{id}").childFolders()
    .buildRequest()
    .get();

```