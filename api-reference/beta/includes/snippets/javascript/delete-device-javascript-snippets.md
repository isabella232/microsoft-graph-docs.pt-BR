---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: d39f0d02f67a4458097b3fbf20855db6f7c29c31
ms.sourcegitcommit: af4b2fc18449c33979cf6d75bd680f40602ba708
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "48610481"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/devices/{id}')
    .version('beta')
    .delete();

```