---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 4abe5a035ed00a51a9be96ab87aa438da453b1ab
ms.sourcegitcommit: 5575e6607817ba23ceb0b01e2f5fc81e58bdcd1f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/22/2020
ms.locfileid: "43718636"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/policies/tokenLifetimePolicies/{id}/appliesTo')
    .get();

```