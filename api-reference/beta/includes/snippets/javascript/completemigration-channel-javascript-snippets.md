---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 68a7ce59516da5d82b9700a0bd04bda223e02e1f
ms.sourcegitcommit: 82da4012294b046416c9ae93d2294d80dab217f6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "48903963"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/teams/{teamId}/channels/{channelId}/completeMigration')
    .version('beta')
    .post();

```