---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: ff48ecd82c2db246e48a8794a032d4301f7627dc
ms.sourcegitcommit: af4b2fc18449c33979cf6d75bd680f40602ba708
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "48619298"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/directoryRoleTemplates')
    .version('beta')
    .get();

```