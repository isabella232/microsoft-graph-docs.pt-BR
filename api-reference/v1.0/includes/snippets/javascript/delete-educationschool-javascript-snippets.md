---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: ddf51878d130f5b4a3884147ae84190fde538f80
ms.sourcegitcommit: af4b2fc18449c33979cf6d75bd680f40602ba708
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "48619951"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/education/schools/{school-id}')
    .delete();

```