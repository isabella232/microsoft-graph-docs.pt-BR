---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 09be6cce37496400b52c3e4798f2d33113feec0b
ms.sourcegitcommit: d4114bac58628527611e83e436132c6581a19c52
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/13/2020
ms.locfileid: "35721467"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/me/messages/{id}')
    .version('beta')
    .delete();

```