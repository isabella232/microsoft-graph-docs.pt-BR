---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: dda7defe387808db155517b56a91f36eea63cc08
ms.sourcegitcommit: 60dfb2ad9ef17f2918c4ee34ebb74f63e32ce2d3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/05/2019
ms.locfileid: "37997432"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/drive/root/workbook/worksheets/{id}/range(address='A1:Z10')/visibleView/rows')
    .version('beta')
    .get();

```