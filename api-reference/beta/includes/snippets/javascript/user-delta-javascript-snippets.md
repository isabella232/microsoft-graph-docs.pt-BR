---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: bfdbca0a0c81b8b40fa01d5c0c205f4262e5f9de
ms.sourcegitcommit: 3f7bac952864cfa67f749d902d9897f08534c0e3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/16/2019
ms.locfileid: "35706779"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/users/delta')
    .version('beta')
    .get();

```