---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: f01abeaeb4f046c033526ad8737b291a4ee1c2df
ms.sourcegitcommit: 3f7bac952864cfa67f749d902d9897f08534c0e3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/16/2019
ms.locfileid: "35706974"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/devices')
    .version('beta')
    .get();

```