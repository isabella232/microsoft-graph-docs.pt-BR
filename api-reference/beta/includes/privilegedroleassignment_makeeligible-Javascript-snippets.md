---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: f54fdda89d556fd0476b14f0a185b836da54f4bb
ms.sourcegitcommit: 4fa6b745383bb0c1864b65d612d811d64cdc079f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2019
ms.locfileid: "34443142"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/privilegedRoleAssignments/{id}/makeEligible')
    .version('beta')
    .post();

```