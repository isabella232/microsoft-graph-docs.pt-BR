---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 38a9404283d086545eb642fc9dcf3dee98e54354
ms.sourcegitcommit: 342516a52b69fcda31442b130eb6bd7e2c8a0066
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/10/2020
ms.locfileid: "48962653"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/administrativeUnits/delta')
    .version('beta')
    .get();

```