---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: dd4bd4b547d96252742096699dde71251e50cddc
ms.sourcegitcommit: af4b2fc18449c33979cf6d75bd680f40602ba708
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "48606621"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/education/me/classes')
    .get();

```