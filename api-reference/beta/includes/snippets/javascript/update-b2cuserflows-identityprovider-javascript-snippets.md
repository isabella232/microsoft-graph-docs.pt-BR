---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 9d88964daf3738037f8bb4e461ef711d5e465c0e
ms.sourcegitcommit: 726f20403323be7d267b67c2764ed7c244e02ee1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/02/2020
ms.locfileid: "47329640"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const identityProviders = {
  @odata.id: "https://graph.microsoft.com/beta/identityProviders/{id}"
};

let res = await client.api('/identity/b2cUserFlows/{id}/identityProviders/$ref')
    .version('beta')
    .update(identityProviders);

```