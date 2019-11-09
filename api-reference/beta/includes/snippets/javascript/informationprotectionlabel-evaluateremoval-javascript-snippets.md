---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 83a6d1e1a46bafbe26d9d436a46cfa23aa1fe246
ms.sourcegitcommit: 60dfb2ad9ef17f2918c4ee34ebb74f63e32ce2d3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/05/2019
ms.locfileid: "37995932"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const informationProtectionAction = {
  contentInfo: {
    @odata.type: "#microsoft.graph.contentInfo",
    format@odata.type: "#microsoft.graph.contentFormat",
    format: "default",
    identifier: null,
    state@odata.type: "#microsoft.graph.contentState",
    state: "rest",
    metadata@odata.type: "#Collection(microsoft.graph.keyValuePair)",
    metadata: [
      {
        @odata.type: "#microsoft.graph.keyValuePair",
        name: "MSIP_Label_722a5300-ac39-4c9a-88e3-f54c46676417_Enabled",
        value: "True"
      },
      {
        @odata.type: "#microsoft.graph.keyValuePair",
        name: "MSIP_Label_722a5300-ac39-4c9a-88e3-f54c46676417_Method",
        value: "Standard"
      },
      {
        @odata.type: "#microsoft.graph.keyValuePair",
        name: "MSIP_Label_722a5300-ac39-4c9a-88e3-f54c46676417_SetDate",
        value: "1/1/0001 12:00:00 AM"
      },
      {
        @odata.type: "#microsoft.graph.keyValuePair",
        name: "MSIP_Label_722a5300-ac39-4c9a-88e3-f54c46676417_SiteId",
        value: "cfa4cf1d-a337-4481-aa99-19d8f3d63f7c"
      },
      {
        @odata.type: "#microsoft.graph.keyValuePair",
        name: "MSIP_Label_722a5300-ac39-4c9a-88e3-f54c46676417_Name",
        value: "General"
      },
      {
        @odata.type: "#microsoft.graph.keyValuePair",
        name: "MSIP_Label_722a5300-ac39-4c9a-88e3-f54c46676417_ContentBits",
        value: "0"
      },
      {
        @odata.type: "#microsoft.graph.keyValuePair",
        name: "MSIP_Label_722a5300-ac39-4c9a-88e3-f54c46676417_ActionId",
        value: "00000000-0000-0000-0000-000000000000"
      }
    ]
  },
  downgradeJustification: {
        justificationMessage: "The information has been declassified.",
        isDowngradeJustified: true
    }
};

let res = await client.api('/informationprotection/policy/labels/evaluateRemoval')
    .version('beta')
    .post(informationProtectionAction);

```