---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: cab34c993fb0b7cb05e265a7050b1d6773ad8aa3
ms.sourcegitcommit: d8a425766aa6a56027b8576bbec6a9d1ae3e079c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/21/2019
ms.locfileid: "36636384"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const plannerPlan = {
  owner: "ebf3b108-5234-4e22-b93d-656d7dae5874",
  title: "title-value"
};

let res = await client.api('/planner/plans')
    .post(plannerPlan);

```