---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: ab52f9899b1df42a3adeb2c72b17f844b2b0fbfb
ms.sourcegitcommit: af4b2fc18449c33979cf6d75bd680f40602ba708
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "48612477"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/me/findRooms')
    .version('beta')
    .get();

```