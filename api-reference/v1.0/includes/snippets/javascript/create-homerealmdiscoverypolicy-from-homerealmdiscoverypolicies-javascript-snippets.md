---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 5aed4506a8a531516b797d962364fadeedffe8e6
ms.sourcegitcommit: 5575e6607817ba23ceb0b01e2f5fc81e58bdcd1f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/22/2020
ms.locfileid: "43805495"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const homeRealmDiscoveryPolicy = {
  definition: [
    "definition-value"
  ],
  displayName: "displayName-value",
  isOrganizationDefault: true
};

let res = await client.api('/policies/homeRealmDiscoveryPolicies')
    .post(homeRealmDiscoveryPolicy);

```