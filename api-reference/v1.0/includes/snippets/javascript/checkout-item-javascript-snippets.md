---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 724cfcab768aee0597e1692e8003cba3d51efa94
ms.sourcegitcommit: d4114bac58628527611e83e436132c6581a19c52
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/13/2020
ms.locfileid: "43511079"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/drives/{drive-id}/items/{item-id}/checkout')
    .post();

```