---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 74b68eac61a2e2b21ada2e153db9fef7cfa1dffe
ms.sourcegitcommit: 342516a52b69fcda31442b130eb6bd7e2c8a0066
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/10/2020
ms.locfileid: "48952520"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

ActivityBasedTimeoutPolicy activityBasedTimeoutPolicy = new ActivityBasedTimeoutPolicy();
LinkedList<String> definitionList = new LinkedList<String>();
definitionList.add("definition-value");
activityBasedTimeoutPolicy.definition = definitionList;
activityBasedTimeoutPolicy.displayName = "displayName-value";
activityBasedTimeoutPolicy.isOrganizationDefault = true;

graphClient.policies().activityBasedTimeoutPolicies()
    .buildRequest()
    .post(activityBasedTimeoutPolicy);

```