---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 3371c83968ebbae09dde320251103a9f41c31b19
ms.sourcegitcommit: a9f0fde9924ad184d315bb2de43c2610002409f3
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/30/2020
ms.locfileid: "48314494"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/teams/{teamsId}/members')
    .get();

```