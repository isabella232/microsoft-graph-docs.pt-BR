---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 8ace58afa38bd5e79d168d906a6add5720c4ab78
ms.sourcegitcommit: 4fa6b745383bb0c1864b65d612d811d64cdc079f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2019
ms.locfileid: "34480887"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const event = {
  originalStartTimeZone: "originalStartTimeZone-value",
  originalEndTimeZone: "originalEndTimeZone-value",
  responseStatus: {
    response: "",
    time: "2016-10-19T10:37:00Z"
  },
  uid: "iCalUId-value",
  reminderMinutesBeforeStart: 99,
  isReminderOn: true
};

let res = await client.api('/groups/{id}/events')
    .version('beta')
    .post({event : event});

```