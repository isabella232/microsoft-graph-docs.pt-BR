---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 1c8f2ae8d0801ad636c9dd39dbd44be28b0e05b1
ms.sourcegitcommit: af4b2fc18449c33979cf6d75bd680f40602ba708
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "48614975"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const convertIdResult = {
  "inputIds" : [
    "{rest-formatted-id-1}",
    "{rest-formatted-id-2}"
  ],
  sourceIdType: "restId",
  targetIdType: "restImmutableEntryId"
};

let res = await client.api('/me/translateExchangeIds')
    .version('beta')
    .post(convertIdResult);

```