---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 5341f88326a350423c94835c6a474f90927a20fa
ms.sourcegitcommit: af4b2fc18449c33979cf6d75bd680f40602ba708
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "48609272"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/me/onenote/sectionGroups/{id}')
    .version('beta')
    .get();

```