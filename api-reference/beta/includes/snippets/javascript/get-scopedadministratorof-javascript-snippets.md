---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 965e19c0f0b186dd5489223c2e0a5a0a58d1147f
ms.sourcegitcommit: ef47b165f7a140cfc0309a275cb8722dd265660d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/25/2020
ms.locfileid: "46873812"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/me/scopedRoleMemberOf')
    .version('beta')
    .get();

```