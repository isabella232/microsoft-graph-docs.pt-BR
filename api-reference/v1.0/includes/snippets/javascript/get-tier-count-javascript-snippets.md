---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: c7d429ad08a060161982eee42d975e11a40696ca
ms.sourcegitcommit: 82da4012294b046416c9ae93d2294d80dab217f6
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "48904278"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/users/{id}/transitiveMemberOf/microsoft.graph.group')
    .header('ConsistencyLevel','eventual')
    .search('displayName:tier')
    .select('displayName,id')
    .orderby('displayName ')
    .get();

```