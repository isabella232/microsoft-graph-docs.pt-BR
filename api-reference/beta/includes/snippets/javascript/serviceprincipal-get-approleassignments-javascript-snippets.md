---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: c84f402880447fcd45871f924ea56908cec1f58f
ms.sourcegitcommit: 5a1373f2ccd9ee813fc60d42e7ac6b115b5f9f66
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/21/2020
ms.locfileid: "44336655"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/servicePrincipals/{id}/appRoleAssignments')
    .version('beta')
    .get();

```