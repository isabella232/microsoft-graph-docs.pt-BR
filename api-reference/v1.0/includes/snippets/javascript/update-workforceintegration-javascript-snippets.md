---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: ccbbb3e74dd0ce7ebe0fd243520e628f27ea99ba
ms.sourcegitcommit: 94c8985a3956622ea90f7e641f894d57b0982eb9
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/02/2020
ms.locfileid: "44218080"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const workforceIntegrations = {
  displayName: "displayName-value",
  apiVersion: 99,
  encryption: {
    protocol: "protocol-value",
    secret: "secret-value"
  },
  isActive: true,
  url: "url-value",
  supportedEntities: "supportedEntities-value"
};

let res = await client.api('/teamwork/workforceIntegrations')
    .update(workforceIntegrations);

```