---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 26cfd7e7bc104a6fbbccc9994b29e8d70956c6d0
ms.sourcegitcommit: af4b2fc18449c33979cf6d75bd680f40602ba708
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "48607358"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/organization')
    .version('beta')
    .get();

```