---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 04f4e147ce5e749ab28515df3fd0a1a4d02ce631
ms.sourcegitcommit: 342516a52b69fcda31442b130eb6bd7e2c8a0066
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/10/2020
ms.locfileid: "48971014"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

LanguageProficiency languageProficiency = graphClient.me().profile().languages("{id}")
    .buildRequest()
    .get();

```