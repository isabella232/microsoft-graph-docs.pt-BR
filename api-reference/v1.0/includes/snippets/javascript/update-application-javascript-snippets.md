---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 4c7a413dc13e9285e0c795ea1108ca388b7bede4
ms.sourcegitcommit: 60dfb2ad9ef17f2918c4ee34ebb74f63e32ce2d3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/05/2019
ms.locfileid: "37995959"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const application = {
  displayName: "New display name"
};

let res = await client.api('/applications/{id}')
    .update(application);

```