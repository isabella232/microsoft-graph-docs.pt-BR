---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: d565b4531565e2422129881e7b421e619f3b5ba2
ms.sourcegitcommit: 2f78ac96a9b0462626a242429055ef824590bd3f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/23/2020
ms.locfileid: "41496763"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/drive/items/{id}/workbook/comments/{id}/replies')
    .get();

```