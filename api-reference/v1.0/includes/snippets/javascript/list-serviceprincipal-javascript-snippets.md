---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 10c1c7b219edfc1ae8a138cb7f9c8c200af1d2fa
ms.sourcegitcommit: 82da4012294b046416c9ae93d2294d80dab217f6
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "48905486"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/servicePrincipals')
    .get();

```