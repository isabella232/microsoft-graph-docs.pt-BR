---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 811f8ac04c789f05ee995d9dc6e288d3910aff90
ms.sourcegitcommit: 5575e6607817ba23ceb0b01e2f5fc81e58bdcd1f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/22/2020
ms.locfileid: "43805362"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

TokenIssuancePolicy tokenIssuancePolicy = new TokenIssuancePolicy();
LinkedList<String> definitionList = new LinkedList<String>();
definitionList.add("definition-value");
tokenIssuancePolicy.definition = definitionList;
tokenIssuancePolicy.displayName = "displayName-value";
tokenIssuancePolicy.isOrganizationDefault = true;

graphClient.policies().tokenIssuancePolicies()
    .buildRequest()
    .post(tokenIssuancePolicy);

```