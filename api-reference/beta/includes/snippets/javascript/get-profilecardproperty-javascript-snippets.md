---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 63539cca46837363cba6a70d1b62b1fba4c85d88
ms.sourcegitcommit: 2c8a12389b82ee5101b2bd17eae11b42e65e52c0
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "45142559"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/organization/{organizationId}/settings/profileCardProperties/{id}')
    .version('beta')
    .get();

```