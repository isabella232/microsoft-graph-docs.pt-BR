---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 137364dfffbc6403aba1035564f2f4d6531b649b
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/02/2019
ms.locfileid: "35518304"
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