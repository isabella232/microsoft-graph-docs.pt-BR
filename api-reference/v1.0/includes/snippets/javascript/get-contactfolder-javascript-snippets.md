---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: c80220f480267cbe206af90b28b8bb5900281e4d
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/02/2019
ms.locfileid: "35507508"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/me/contactFolders/{id}')
    .get();

```