---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 75c9b50135879067bacce7aff8030351c11c14b5
ms.sourcegitcommit: 4fa6b745383bb0c1864b65d612d811d64cdc079f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2019
ms.locfileid: "34434333"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/me/calendarGroups/{id}')
    .get();

```