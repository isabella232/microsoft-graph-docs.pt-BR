---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 0639d797392ce69ecb8d16672e113df9534234c9
ms.sourcegitcommit: 82da4012294b046416c9ae93d2294d80dab217f6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "48905945"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/contacts')
    .header('ConsistencyLevel','eventual')
    .search('displayName:wa')
    .get();

```