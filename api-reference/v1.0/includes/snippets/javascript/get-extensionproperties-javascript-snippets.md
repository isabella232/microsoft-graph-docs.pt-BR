---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 1203c5653f27272083d4aae39ccbc8e48bf76f9b
ms.sourcegitcommit: 60dfb2ad9ef17f2918c4ee34ebb74f63e32ce2d3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/05/2019
ms.locfileid: "37999142"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/applications/{id}/extensionProperties')
    .get();

```