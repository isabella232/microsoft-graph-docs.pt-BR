---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: b8d123c7b4b1a2c81166f6e0cb0a0395f9591ddf
ms.sourcegitcommit: 496410c1e256aa093eabf27f17e820d9ee91a293
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/05/2020
ms.locfileid: "46565806"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/termStore')
    .version('beta')
    .get();

```