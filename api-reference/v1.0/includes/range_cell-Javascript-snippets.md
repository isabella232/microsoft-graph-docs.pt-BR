---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: c20ac73b38f3a8d406927f0494391d8d9bba6f66
ms.sourcegitcommit: 4fa6b745383bb0c1864b65d612d811d64cdc079f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2019
ms.locfileid: "34452767"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/me/drive/items/{id}/workbook/names/{name}/range/cell(row=5,column=6)')
    .get();

```