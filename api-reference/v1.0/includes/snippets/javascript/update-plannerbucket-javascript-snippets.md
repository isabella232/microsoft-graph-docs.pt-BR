---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: c4bb47a5b330f4056e5d3a28ba67600e0f2e4d61
ms.sourcegitcommit: 0329bbcd5f1b09a2a6c5f935a30c4560b6eed492
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2019
ms.locfileid: "36636381"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const plannerBucket = {
  name: "Development"
};

let res = await client.api('/planner/buckets/{bucket-id}')
    .update(plannerBucket);

```