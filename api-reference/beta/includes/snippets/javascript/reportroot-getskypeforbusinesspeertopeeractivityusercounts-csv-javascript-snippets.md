---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: dbb5aa9929e5e8fd1cabdc35434b297c0e3e0141
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/02/2019
ms.locfileid: "35518665"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/reports/getSkypeForBusinessPeerToPeerActivityUserCounts(period='D7')')
    .version('beta')
    .get();

```