---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: dcd7af564d29a573dfeded8931de0a01394cbc9b
ms.sourcegitcommit: 82da4012294b046416c9ae93d2294d80dab217f6
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "48903657"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/groups/{id}/members/microsoft.graph.user/$count')
    .header('ConsistencyLevel','eventual')
    .get();

```