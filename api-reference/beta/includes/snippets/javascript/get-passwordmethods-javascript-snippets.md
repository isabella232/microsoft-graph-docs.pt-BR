---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 383939182ce5d1070d5f649d45f65ccb8cf6c2d0
ms.sourcegitcommit: 5575e6607817ba23ceb0b01e2f5fc81e58bdcd1f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/22/2020
ms.locfileid: "43805887"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/me/authentication/passwordMethods')
    .version('beta')
    .get();

```