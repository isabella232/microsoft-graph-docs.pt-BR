---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: f1a758ee41876456fc8504f422a00779f64ae54d
ms.sourcegitcommit: af4b2fc18449c33979cf6d75bd680f40602ba708
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "48604249"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/me/drive/items/{id}/workbook/tables/{id|name}')
    .get();

```