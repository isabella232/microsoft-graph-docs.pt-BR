---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: ef056e74ac90300062cb0ec631d1a2b3b8e7aa66
ms.sourcegitcommit: 3f7bac952864cfa67f749d902d9897f08534c0e3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/16/2019
ms.locfileid: "35710957"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/accessReviews/2b83cc42-09db-46f6-8c6e-16fec466a82d')
    .version('beta')
    .get();

```