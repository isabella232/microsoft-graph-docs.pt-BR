---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: f64fe29b144413d4be950a9a2e53d2e996fd3dae
ms.sourcegitcommit: d8a58221ed1f2b7b7073fd621da4737e11ba53c5
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/11/2019
ms.locfileid: "36839099"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/drive/root/workbook/comments')
    .get();

```