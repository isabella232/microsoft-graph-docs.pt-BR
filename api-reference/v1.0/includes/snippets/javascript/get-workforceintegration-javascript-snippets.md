---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: ced5764a96549a7e7f7ceaa71831b16bfe101a7b
ms.sourcegitcommit: d4114bac58628527611e83e436132c6581a19c52
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/13/2020
ms.locfileid: "44217040"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/teamwork/workforceIntegrations/{workforceintegrationid}')
    .get();

```