---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: eb7e6835b69bd57dc63ee7a3deffe42aba30da8e
ms.sourcegitcommit: f27e81daeff242e623d1a3627405667310395734
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/25/2019
ms.locfileid: "40871052"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const changeScreenSharingRole = {
  role: "viewer"
};

let res = await client.api('/communications/calls/{id}/changeScreenSharingRole')
    .post(changeScreenSharingRole);

```