---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 50155f71279f49080af201820d620a51fe875e95
ms.sourcegitcommit: 3f7bac952864cfa67f749d902d9897f08534c0e3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/16/2019
ms.locfileid: "35714968"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/me/mailboxSettings')
    .get();

```