---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 07773e6296b594551f743825a42da1b651f4bf85
ms.sourcegitcommit: af4b2fc18449c33979cf6d75bd680f40602ba708
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "48614217"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/me/drive/root')
    .version('beta')
    .get();

```