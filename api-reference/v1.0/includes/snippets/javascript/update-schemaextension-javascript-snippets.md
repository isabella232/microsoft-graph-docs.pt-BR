---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: bd9d53bd362eced1ab6918e8d6fa92f47471daba
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/02/2019
ms.locfileid: "35492329"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const schemaExtension = {
  properties: [
    {
      name:"new-name-value",
      type:"new-type-value"
    },
    {
      name:"additional-name-value",
      type:"additional-type-value"
    }
  ],
};

let res = await client.api('/schemaExtensions/{id}')
    .update({schemaExtension : schemaExtension});

```