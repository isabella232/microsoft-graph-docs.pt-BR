---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 137364dfffbc6403aba1035564f2f4d6531b649b
ms.sourcegitcommit: 4fa6b745383bb0c1864b65d612d811d64cdc079f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2019
ms.locfileid: "34442631"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/me/drive/items/{id}/workbook/names/{name}/range/format/autofitColumns')
    .version('beta')
    .post();

```