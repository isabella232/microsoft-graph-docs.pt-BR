---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: adf7c1b1fa1189413a3a9cd7442dc33525c40240
ms.sourcegitcommit: f27e81daeff242e623d1a3627405667310395734
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/25/2019
ms.locfileid: "37999071"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/applications/{id}/owners/{id}/$ref')
    .delete();

```