---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: e7d993e40f582f9b2e95f22608d72876d24a8e81
ms.sourcegitcommit: b18f978808fef800bff9e587464a5f3e18eb7687
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/25/2019
ms.locfileid: "35885008"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/me/messages/{id}/attachments')
    .get();

```