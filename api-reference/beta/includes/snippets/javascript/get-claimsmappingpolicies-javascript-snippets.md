---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: bfb5f1e521a738325fb47a8363d0dd4a29857b26
ms.sourcegitcommit: 2f78ac96a9b0462626a242429055ef824590bd3f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/23/2020
ms.locfileid: "41476361"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/policies/claimsMappingPolicies')
    .version('beta')
    .get();

```