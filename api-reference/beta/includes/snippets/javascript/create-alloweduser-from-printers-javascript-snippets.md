---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 2e8063ec8c3b8aad05ff4cdffed545f154429003
ms.sourcegitcommit: d4114bac58628527611e83e436132c6581a19c52
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/13/2020
ms.locfileid: "44216760"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const printUserIdentity = {
  @odata.id: "https://graph.microsoft.com/beta/users/{id}"
};

let res = await client.api('/print/shares/{id}/allowedUsers/$ref')
    .version('beta')
    .post(printUserIdentity);

```