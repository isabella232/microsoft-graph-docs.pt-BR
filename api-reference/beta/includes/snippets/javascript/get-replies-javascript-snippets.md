---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: c9b653ee3352f0ca59df8f0e65fe4fe72d7a137d
ms.sourcegitcommit: 2f78ac96a9b0462626a242429055ef824590bd3f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/23/2020
ms.locfileid: "41495998"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/drive/items/{id}/workbook/comments/{id}/replies')
    .version('beta')
    .get();

```