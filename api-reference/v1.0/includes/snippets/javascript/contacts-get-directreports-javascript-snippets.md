---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: bfc43bec5671bfebff80760cb9222b2dd9a411c6
ms.sourcegitcommit: 3ee6a3a949be7f0a9028bde90092a10a42e0f1fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/23/2019
ms.locfileid: "37638057"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/contacts/{id}/directReports')
    .get();

```