---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 762a6cd49d9354ed591267feb2844c854879b282
ms.sourcegitcommit: af4b2fc18449c33979cf6d75bd680f40602ba708
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "48613731"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/education/classes/11022')
    .version('beta')
    .delete();

```