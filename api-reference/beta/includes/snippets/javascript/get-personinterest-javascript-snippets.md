---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 3132c426bb7130da75d4b2bbe6cdc3901e1bf9de
ms.sourcegitcommit: 239db9e961e42b505f52de9859963a9136935f2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "46819629"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/me/profile/interests/{id}')
    .version('beta')
    .get();

```