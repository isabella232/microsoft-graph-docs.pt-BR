---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 63ee4963e5e8844cfbf7d45e637200c8d47907cd
ms.sourcegitcommit: 4fa6b745383bb0c1864b65d612d811d64cdc079f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2019
ms.locfileid: "34455637"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/me/mailFolders/delta')
    .get();

```