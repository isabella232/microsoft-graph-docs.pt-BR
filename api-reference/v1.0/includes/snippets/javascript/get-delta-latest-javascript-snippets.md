---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 3eb9024bc3b355fb4f48f4418bd79a2f6042a68f
ms.sourcegitcommit: af4b2fc18449c33979cf6d75bd680f40602ba708
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "48609717"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/me/drive/root/delta?token=latest')
    .get();

```