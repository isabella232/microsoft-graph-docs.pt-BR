---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 04a45659c47f1f5457f6a5d2b3bd22921acaf6b6
ms.sourcegitcommit: 3f7bac952864cfa67f749d902d9897f08534c0e3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/16/2019
ms.locfileid: "35732845"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/me/drive/items/{item-id}/permissions/{perm-id}')
    .delete();

```