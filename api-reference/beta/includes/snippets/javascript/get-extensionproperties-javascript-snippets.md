---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 93251e222308db629c33b7638f5765776c9ca044
ms.sourcegitcommit: 60dfb2ad9ef17f2918c4ee34ebb74f63e32ce2d3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/05/2019
ms.locfileid: "37995448"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/applications/{id}/extensionProperties')
    .version('beta')
    .get();

```