---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: b8edb3a31ae5e0132b784e96bfd169856d8bda7b
ms.sourcegitcommit: 3f7bac952864cfa67f749d902d9897f08534c0e3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/16/2019
ms.locfileid: "35708933"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/app/calls/{id}/audioRoutingGroups')
    .version('beta')
    .get();

```