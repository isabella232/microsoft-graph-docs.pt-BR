---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 3874501ecd3b5c90e8cb0a6ebbc428c479f10d70
ms.sourcegitcommit: af4b2fc18449c33979cf6d75bd680f40602ba708
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "48613884"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/me/calendarGroups')
    .version('beta')
    .get();

```