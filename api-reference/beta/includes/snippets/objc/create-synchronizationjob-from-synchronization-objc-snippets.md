---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 60e3f0271b7a794d5a096f3cefb2697a947f1089
ms.sourcegitcommit: af4b2fc18449c33979cf6d75bd680f40602ba708
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "48615064"
---
```objc

MSHTTPClient *httpClient = [MSClientFactory createHTTPClientWithAuthenticationProvider:authenticationProvider];

NSString *MSGraphBaseURL = @"https://graph.microsoft.com/beta/";
NSMutableURLRequest *urlRequest = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:[MSGraphBaseURL stringByAppendingString:@"/servicePrincipals/{id}/synchronization/jobs"]]];
[urlRequest setHTTPMethod:@"POST"];
[urlRequest setValue:@"application/json" forHTTPHeaderField:@"Content-Type"];

MSGraphSynchronizationJob *synchronizationJob = [[MSGraphSynchronizationJob alloc] init];
[synchronizationJob setTemplateId:@"BoxOutDelta"];

NSError *error;
NSData *synchronizationJobData = [synchronizationJob getSerializedDataWithError:&error];
[urlRequest setHTTPBody:synchronizationJobData];

MSURLSessionDataTask *meDataTask = [httpClient dataTaskWithRequest:urlRequest 
    completionHandler: ^(NSData *data, NSURLResponse *response, NSError *nserror) {

        //Request Completed

}];

[meDataTask execute];

```