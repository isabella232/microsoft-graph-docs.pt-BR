---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: be2c7f844559336ce99bee3f2200fa2554255b59
ms.sourcegitcommit: 60dfb2ad9ef17f2918c4ee34ebb74f63e32ce2d3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/05/2019
ms.locfileid: "37998578"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/me/profile/emails/{id}')
    .version('beta')
    .get();

```