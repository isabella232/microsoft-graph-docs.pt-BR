---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: d37afe32df2ba4f4a54502016cab9296788c3311
ms.sourcegitcommit: b18f978808fef800bff9e587464a5f3e18eb7687
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/25/2019
ms.locfileid: "35874156"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/reports/getCredentialUsageSummary(period='D30')')
    .version('beta')
    .filter('feature eq 'registration'')
    .get();

```