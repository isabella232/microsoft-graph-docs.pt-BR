---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 3b674fa5a3274d3f03f37c3ee178d847a46ec67e
ms.sourcegitcommit: 4fa6b745383bb0c1864b65d612d811d64cdc079f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2019
ms.locfileid: "34452739"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const clear = {
  applyTo: "applyTo-value"
};

let res = await client.api('/me/drive/items/{id}/workbook/names/{name}/range/clear')
    .post(clear);

```