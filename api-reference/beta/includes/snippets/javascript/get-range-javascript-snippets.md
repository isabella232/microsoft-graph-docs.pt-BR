---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 5fa9271110e386c2d906a1b1b8c6274850e8b700
ms.sourcegitcommit: af4b2fc18449c33979cf6d75bd680f40602ba708
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "48603725"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/me/drive/items/{id}/workbook/names/{name}/range')
    .version('beta')
    .get();

```