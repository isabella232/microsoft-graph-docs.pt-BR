---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: d8d5a85865f6b653e9532605d67a5cb98ddcb105
ms.sourcegitcommit: 726f20403323be7d267b67c2764ed7c244e02ee1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/02/2020
ms.locfileid: "47329965"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const b2cIdentityUserFlow = {
    id: "Customer",
    userFlowType: "signUpOrSignIn",
    userFlowTypeVersion: 3
};

let res = await client.api('/identity/b2cUserFlows')
    .version('beta')
    .post(b2cIdentityUserFlow);

```