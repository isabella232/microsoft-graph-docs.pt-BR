---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: aa88ee3ebe9d140cf4bd6357f82075d772e68b9a
ms.sourcegitcommit: af4b2fc18449c33979cf6d75bd680f40602ba708
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "48615024"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/directory/deleteditems/46cc6179-19d0-473e-97ad-6ff84347bbbb')
    .version('beta')
    .get();

```