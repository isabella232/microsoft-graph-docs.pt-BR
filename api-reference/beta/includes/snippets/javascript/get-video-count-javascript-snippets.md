---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: a12e07c563ec4bc0e1335557218ca9e18c4cbbd5
ms.sourcegitcommit: c20276369a8834a259f24038e7ee5c33de02660b
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/07/2020
ms.locfileid: "48375666"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/groups/{id}/memberOf/microsoft.graph.group')
    .version('beta')
    .header('ConsistencyLevel','eventual')
    .search('displayName:Video')
    .orderby('displayName ')
    .get();

```