---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 204e8e45355d4fcb15a864c5faaf5029aa96b77a
ms.sourcegitcommit: af4b2fc18449c33979cf6d75bd680f40602ba708
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "48615309"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/me/drive/items/{id}/workbook/worksheets/{id|name}/charts')
    .get();

```