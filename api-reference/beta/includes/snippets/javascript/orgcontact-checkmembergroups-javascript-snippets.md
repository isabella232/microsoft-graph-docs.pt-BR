---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 30b65d8827011cb784eeae8ea2efc6648bc2e590
ms.sourcegitcommit: 1585d55d3e7030b5fd1f7cfd5de8f9fb8202cd56
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2019
ms.locfileid: "37428733"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const string = {
  groupIds: [
    "groupIds-value"
  ]
};

let res = await client.api('/contacts/{id}/checkMemberGroups')
    .version('beta')
    .post(string);

```