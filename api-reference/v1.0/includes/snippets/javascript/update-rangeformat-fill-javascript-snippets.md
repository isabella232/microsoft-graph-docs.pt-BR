---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: b9bfc0e32c4a29f2e8372ae6a978f32e47726e2c
ms.sourcegitcommit: 0329bbcd5f1b09a2a6c5f935a30c4560b6eed492
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2019
ms.locfileid: "36636360"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const workbookRangeFill = {
  color: "#FF0000"
};

let res = await client.api('/me/drive/items/{id}/workbook/worksheets/{sheet-id}/range(address='$A$1')/format/fill')
    .update(workbookRangeFill);

```