---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: b5661e963ca7660c3333581d17dd6cb1fad5456d
ms.sourcegitcommit: 2f78ac96a9b0462626a242429055ef824590bd3f
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/23/2020
ms.locfileid: "41558988"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/me/messages/4aade2547798441eab5188a7a2436bc1/$value')
    .get();

```