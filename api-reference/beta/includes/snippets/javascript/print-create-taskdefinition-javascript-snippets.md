---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 766b009204810fb8472e80dfc45552877a08e962
ms.sourcegitcommit: 496410c1e256aa093eabf27f17e820d9ee91a293
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/05/2020
ms.locfileid: "46566408"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const printTaskDefinition = {
  displayName: "Test TaskDefinitionName",
  createdBy: {
    displayName: "Requesting App Display Name"
  }
};

let res = await client.api('/print/taskDefinitions')
    .version('beta')
    .post(printTaskDefinition);

```