---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 4263a9db2cdbe310b16a4c163fcf05963e71f951
ms.sourcegitcommit: 342516a52b69fcda31442b130eb6bd7e2c8a0066
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/10/2020
ms.locfileid: "48962946"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/directoryRoles/{id}/members/{id}/$ref')
    .version('beta')
    .delete();

```