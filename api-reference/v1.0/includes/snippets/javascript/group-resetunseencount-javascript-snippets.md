---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: a76a6b4a593649c1fdcccb496e5b19a8e24d4041
ms.sourcegitcommit: af4b2fc18449c33979cf6d75bd680f40602ba708
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "48606094"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/groups/{id}/resetUnseenCount')
    .post();

```