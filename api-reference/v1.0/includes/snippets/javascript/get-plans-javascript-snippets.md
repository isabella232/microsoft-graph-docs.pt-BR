---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: d3d42929f6d53c7cdbe3ef91637022cf5d8a862e
ms.sourcegitcommit: af4b2fc18449c33979cf6d75bd680f40602ba708
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "48616858"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/me/planner/plans')
    .get();

```