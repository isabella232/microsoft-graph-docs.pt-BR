---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: b4a14a02d551f20e8387c8c1895eb124a45967cc
ms.sourcegitcommit: 3f7bac952864cfa67f749d902d9897f08534c0e3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/16/2019
ms.locfileid: "35705147"
---
```objc

MSHTTPClient *httpClient = [MSClientFactory createHTTPClientWithAuthenticationProvider:authenticationProvider];

NSString *MSGraphBaseURL = @"https://graph.microsoft.com/v1.0/";
NSMutableURLRequest *urlRequest = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:[MSGraphBaseURL stringByAppendingString:@"/planner/tasks/{task-id}/assignedToTaskBoardFormat"]]];
[urlRequest setHTTPMethod:@"GET"];

MSURLSessionDataTask *meDataTask = [httpClient dataTaskWithRequest:urlRequest 
    completionHandler: ^(NSData *data, NSURLResponse *response, NSError *nserror) {

        MSGraphPlannerAssignedToTaskBoardTaskFormat *plannerAssignedToTaskBoardTaskFormat = [[MSGraphPlannerAssignedToTaskBoardTaskFormat alloc] initWithData:data error:&nserror];

}];

[meDataTask execute];

```