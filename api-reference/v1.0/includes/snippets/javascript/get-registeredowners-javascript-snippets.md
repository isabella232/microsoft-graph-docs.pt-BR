---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 83f44945f15bf60c136df37742f2cc8d614c20d8
ms.sourcegitcommit: af4b2fc18449c33979cf6d75bd680f40602ba708
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "48612040"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/devices/{id}/registeredOwners')
    .get();

```