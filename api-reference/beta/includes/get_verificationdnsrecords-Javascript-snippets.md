---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: bc7443848049372502b239fae20d9fc0c5773eb2
ms.sourcegitcommit: 4fa6b745383bb0c1864b65d612d811d64cdc079f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2019
ms.locfileid: "34445112"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/domains/contoso.com/verificationDnsRecords')
    .version('beta')
    .get();

```