---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: f2357dd3e71556f664e627fbb0cb3f86b405da81
ms.sourcegitcommit: 0545b031585e605dc3a0fde481015f51f79819c4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/22/2020
ms.locfileid: "45224543"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const directoryObject = {
  @odata.id: "https://graph.microsoft.com/v1.0/directoryObjects/{id}"
};

let res = await client.api('/devices/{id}/registeredUsers/$ref')
    .post(directoryObject);

```