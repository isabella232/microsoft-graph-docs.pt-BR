---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: c2efaa8b1c58d02d615af1f1dd63ddf9402954f0
ms.sourcegitcommit: 5f643d3b3f71a9711963c8953da2188539fc9b0c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/14/2020
ms.locfileid: "41119510"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/accessReviews')
    .version('beta')
    .filter('businessFlowTemplateId+eq+'6e4f3d20-c5c3-407f-9695-8460952bcc68',')
    .skip(0)
    .top(100)
    .get();

```