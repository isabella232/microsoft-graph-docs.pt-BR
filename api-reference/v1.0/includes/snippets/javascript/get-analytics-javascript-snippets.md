---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 267c0f8a6f5024928fc684ae971b9e254ebc8a75
ms.sourcegitcommit: d4114bac58628527611e83e436132c6581a19c52
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/13/2020
ms.locfileid: "44052314"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/me/followedSites')
    .post();

```