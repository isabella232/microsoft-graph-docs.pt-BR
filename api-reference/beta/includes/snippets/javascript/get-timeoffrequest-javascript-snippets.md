---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: f243e82eadeabc0931084cbbb74be1f1760ab267
ms.sourcegitcommit: 94c8985a3956622ea90f7e641f894d57b0982eb9
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/02/2020
ms.locfileid: "44217047"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/teams/{teamId}/schedule/timeOffRequests')
    .version('beta')
    .get();

```