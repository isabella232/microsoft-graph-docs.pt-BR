---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: a495d4843ddee546a05281bd66cffa4014d434b4
ms.sourcegitcommit: 60dfb2ad9ef17f2918c4ee34ebb74f63e32ce2d3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/05/2019
ms.locfileid: "37994183"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/identityGovernance/entitlementManagement/accessPackages/{id}')
    .version('beta')
    .expand('accessPackageResourceRoleScopes($expand=accessPackageResourceRole,accessPackageResourceScope)')
    .get();

```