---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: adf7c1b1fa1189413a3a9cd7442dc33525c40240
ms.sourcegitcommit: 60dfb2ad9ef17f2918c4ee34ebb74f63e32ce2d3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/05/2019
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