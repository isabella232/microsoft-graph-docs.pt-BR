---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: cb8d13be34562c90e8b3644b66e5dfce2de4b969
ms.sourcegitcommit: af4b2fc18449c33979cf6d75bd680f40602ba708
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "48613718"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/trustFramework/policies/B2C_1A_SocialAndLocalAccounts_Base')
    .version('beta')
    .delete();

```