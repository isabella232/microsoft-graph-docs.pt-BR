---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 609515bd0b2e0b5168076c4210d68875c91f1143
ms.sourcegitcommit: 0329bbcd5f1b09a2a6c5f935a30c4560b6eed492
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2019
ms.locfileid: "36636256"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const synchronizationJob = {
    templateId: "BoxOutDelta"
};

let res = await client.api('/servicePrincipals/{id}/synchronization/jobs')
    .version('beta')
    .post(synchronizationJob);

```