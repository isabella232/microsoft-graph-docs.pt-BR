---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 36bb2d3d2a8b2317fc41f1fae6a1c4b53b6289c2
ms.sourcegitcommit: af4b2fc18449c33979cf6d75bd680f40602ba708
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "48610887"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/groups/{id}/subscribeByMail')
    .version('beta')
    .post();

```