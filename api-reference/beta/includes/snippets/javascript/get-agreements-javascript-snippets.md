---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: a817c3b3cfdc0da926a18eba75709d3a57535380
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/02/2019
ms.locfileid: "35519419"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/agreements')
    .version('beta')
    .get();

```