---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 2817d942a6b164cfab95caae9caaff979d06de6f
ms.sourcegitcommit: af4b2fc18449c33979cf6d75bd680f40602ba708
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "48606555"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/users/{idOrUserPrincipalName}/drive')
    .get();

```