---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 29285b8bcccc37e97fc6c996b70d0477c03eb281
ms.sourcegitcommit: 94c8985a3956622ea90f7e641f894d57b0982eb9
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/02/2020
ms.locfileid: "44215812"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/teams/{teamId}/schedule/timeOffRequests')
    .get();

```