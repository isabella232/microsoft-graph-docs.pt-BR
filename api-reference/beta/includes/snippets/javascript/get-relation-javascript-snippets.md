---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: cbc0ca987f79e95689b29df5a6c85968816936d0
ms.sourcegitcommit: 726f20403323be7d267b67c2764ed7c244e02ee1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/02/2020
ms.locfileid: "47330225"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/termStore/sets/{setId}/relations')
    .version('beta')
    .get();

```