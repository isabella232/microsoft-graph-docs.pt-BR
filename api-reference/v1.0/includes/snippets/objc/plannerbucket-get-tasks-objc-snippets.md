---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 4aeb29fef68c1a8f805478d2cfe2ce1a92c913bc
ms.sourcegitcommit: ef8eac3cf973a1971f8f1d41d75a085fad3690f0
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/15/2019
ms.locfileid: "37637858"
---
```objc

MSHTTPClient *httpClient = [MSClientFactory createHTTPClientWithAuthenticationProvider:authenticationProvider];

NSString *MSGraphBaseURL = @"https://graph.microsoft.com/v1.0/";
NSMutableURLRequest *urlRequest = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:[MSGraphBaseURL stringByAppendingString:@"/planner/buckets/{task-id}/tasks"]]];
[urlRequest setHTTPMethod:@"GET"];

MSURLSessionDataTask *meDataTask = [httpClient dataTaskWithRequest:urlRequest 
    completionHandler: ^(NSData *data, NSURLResponse *response, NSError *nserror) {

        NSError *jsonError = nil;
        NSDictionary *jsonFinal = [NSJSONSerialization JSONObjectWithData:data options:0 error:&jsonError];
        NSMutableArray *plannerTaskList = [[NSMutableArray alloc] init];
        plannerTaskList = [jsonFinal valueForKey:@"value"];
        MSGraphPlannerTask *plannerTask = [[MSGraphPlannerTask alloc] initWithDictionary:[plannerTaskList objectAtIndex: 0] error:&nserror];

}];

[meDataTask execute];

```