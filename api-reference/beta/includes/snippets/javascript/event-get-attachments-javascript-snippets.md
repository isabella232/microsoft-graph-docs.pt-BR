---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: b31cc05f77b88c74839bbe735da20557d11fdb25
ms.sourcegitcommit: b18f978808fef800bff9e587464a5f3e18eb7687
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/25/2019
ms.locfileid: "35859554"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/me/events/{id}/attachments')
    .version('beta')
    .get();

```