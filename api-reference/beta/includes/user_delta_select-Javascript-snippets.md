---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 24952b8d9451e3c6957f2d6b3fcb2845ffc5954b
ms.sourcegitcommit: 4fa6b745383bb0c1864b65d612d811d64cdc079f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2019
ms.locfileid: "34450374"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/users/delta')
    .version('beta')
    .select('displayName,jobTitle,mobilePhone')
    .get();

```