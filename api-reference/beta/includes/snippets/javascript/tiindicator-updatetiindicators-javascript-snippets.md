---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 791c77ba3afa4971cb654532220e3138f85d61b1
ms.sourcegitcommit: af4b2fc18449c33979cf6d75bd680f40602ba708
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "48618852"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const tiIndicator = {
  value: [
    {
      id: "c6fb948b-89c5-3bba-a2cd-a9d9a1e430e4",
      additionalInformation: "mytest"
    },
    {
      id: "e58c072b-c9bb-a5c4-34ce-eb69af44fb1e",
      additionalInformation: "test again"
    }
  ]
};

let res = await client.api('/security/tiIndicators/updateTiIndicators')
    .version('beta')
    .post(tiIndicator);

```