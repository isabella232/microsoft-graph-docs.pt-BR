---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: dfa1b280625ceaabfb82f2dc06c090ea69f790b3
ms.sourcegitcommit: 7b286637aa332cfd534a41526950b4f6272e0fd7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/05/2020
ms.locfileid: "41774770"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/users/AlexW@contoso.OnMicrosoft.com/calendar/calendarPermissions')
    .version('beta')
    .get();

```