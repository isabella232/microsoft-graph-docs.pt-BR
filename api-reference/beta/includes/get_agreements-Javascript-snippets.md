---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: a817c3b3cfdc0da926a18eba75709d3a57535380
ms.sourcegitcommit: 4fa6b745383bb0c1864b65d612d811d64cdc079f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2019
ms.locfileid: "34474139"
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