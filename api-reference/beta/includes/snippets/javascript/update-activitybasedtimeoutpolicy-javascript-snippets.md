---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 43c782b05ff8a7e01f31135dd1a34ebd0598d0de
ms.sourcegitcommit: c4d6ccd343a6b298a2aa844f1bad66c736487251
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/11/2020
ms.locfileid: "42589772"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const activityBasedTimeoutPolicy = {
  definition: [
    "definition-value"
  ],
  displayName: "displayName-value",
  isOrganizationDefault: true,
  type: "type-value"
};

let res = await client.api('/policies/activityBasedTimeoutPolicies/{id}')
    .version('beta')
    .update(activityBasedTimeoutPolicy);

```