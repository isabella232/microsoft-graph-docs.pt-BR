---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: fe84d9c2ef8fa92d2bc2af38697ee6a9e2f17c4d
ms.sourcegitcommit: af4b2fc18449c33979cf6d75bd680f40602ba708
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "48613819"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/planner/plans/{plan-id}/details')
    .get();

```