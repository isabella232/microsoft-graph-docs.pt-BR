---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 2c29da3595d820b685f5723c2459299ffff33626
ms.sourcegitcommit: d4114bac58628527611e83e436132c6581a19c52
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/13/2020
ms.locfileid: "44216907"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/print/shares/{id}')
    .version('beta')
    .delete();

```