---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: c77530e466edd3e4cbc4f4f60842fb23c21462cc
ms.sourcegitcommit: 8e18d7fe3c869b2fd48872365116175d3bdce1b7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/12/2020
ms.locfileid: "46644973"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const phoneAuthenticationMethod = {
  phoneNumber: "+1 2065555555",
  phoneType: "mobile"
};

let res = await client.api('/me/authentication/phoneMethods')
    .version('beta')
    .post(phoneAuthenticationMethod);

```