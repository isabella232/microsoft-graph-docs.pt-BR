---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: f371cd18527460a1be11c76ebd1963869b682608
ms.sourcegitcommit: 239db9e961e42b505f52de9859963a9136935f2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "46821398"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const personInterest = {
  categories: [
    "Sports"
  ],
  description: "World's greatest football club",
  displayName: "Chelsea FC",
  webUrl: "https://www.chelseafc.com"
};

let res = await client.api('/me/profile/interests')
    .version('beta')
    .post(personInterest);

```