---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 3543fc8f60316c94e9dba4bc25541d7d3e6e87de
ms.sourcegitcommit: 4fa6b745383bb0c1864b65d612d811d64cdc079f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2019
ms.locfileid: "34460900"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const permission = {
  type: "embed"
};

let res = await client.api('/me/drive/items/{item-id}/createLink')
    .version('beta')
    .post(permission);

```