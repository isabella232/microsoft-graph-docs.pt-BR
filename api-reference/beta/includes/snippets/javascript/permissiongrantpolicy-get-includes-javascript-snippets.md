---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 040850b1cc58b0cdb0f8f52464a97020f8bd8531
ms.sourcegitcommit: be796d6a7ae62f052c381d20207545f057b184d9
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/14/2020
ms.locfileid: "48460159"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/policies/permissionGrantPolicies/microsoft-application-admin/includes')
    .version('beta')
    .get();

```