---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 700c54523e44ee74cbf20897358a1ccb23dc923d
ms.sourcegitcommit: 239db9e961e42b505f52de9859963a9136935f2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "46819517"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const itemEmail = {
  address: "Innocenty.Popov@adventureworks.com",
};

let res = await client.api('/me/profile/emails')
    .version('beta')
    .post(itemEmail);

```