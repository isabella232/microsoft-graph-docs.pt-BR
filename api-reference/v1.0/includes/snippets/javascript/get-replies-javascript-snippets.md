---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: e365f738024976d2341d7b7cb8a4119c1b1b2ad2
ms.sourcegitcommit: d8a58221ed1f2b7b7073fd621da4737e11ba53c5
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/11/2019
ms.locfileid: "36839029"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/drive/root/workbook/comments/{id}/replies')
    .get();

```