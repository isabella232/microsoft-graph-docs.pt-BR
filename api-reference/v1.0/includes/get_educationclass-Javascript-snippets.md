---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: a764022f5cdd42f6a51e8b18d2e56cc18ccfac93
ms.sourcegitcommit: 4fa6b745383bb0c1864b65d612d811d64cdc079f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2019
ms.locfileid: "34479592"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/education/classes/{class-id}')
    .get();

```