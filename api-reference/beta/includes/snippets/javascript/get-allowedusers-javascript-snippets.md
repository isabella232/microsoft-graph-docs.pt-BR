---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: c3437452b92d67c6b3206ba4a73c187ea3ec71a2
ms.sourcegitcommit: 33ffed5b785abf36b1a7786856c9266958830d25
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/25/2020
ms.locfileid: "42947888"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/print/printers/{id}/allowedUsers')
    .version('beta')
    .get();

```