---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: c7568fffe52710414afcb0a35dcecfe74abc071e
ms.sourcegitcommit: af4b2fc18449c33979cf6d75bd680f40602ba708
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "48610586"
---
```objc

MSHTTPClient *httpClient = [MSClientFactory createHTTPClientWithAuthenticationProvider:authenticationProvider];

NSString *MSGraphBaseURL = @"https://graph.microsoft.com/v1.0/";
NSMutableURLRequest *urlRequest = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:[MSGraphBaseURL stringByAppendingString:@"/devices"]]];
[urlRequest setHTTPMethod:@"POST"];
[urlRequest setValue:@"application/json" forHTTPHeaderField:@"Content-Type"];

MSGraphDevice *device = [[MSGraphDevice alloc] init];
[device setAccountEnabled: false];
NSMutableArray *alternativeSecurityIdsList = [[NSMutableArray alloc] init];
MSGraphAlternativeSecurityId *alternativeSecurityIds = [[MSGraphAlternativeSecurityId alloc] init];
[alternativeSecurityIds setType: 2];
[alternativeSecurityIds setKey:@"base64Y3YxN2E1MWFlYw=="];
[alternativeSecurityIdsList addObject: alternativeSecurityIds];
[device setAlternativeSecurityIds:alternativeSecurityIdsList];
[device setDeviceId:@"4c299165-6e8f-4b45-a5ba-c5d250a707ff"];
[device setDisplayName:@"Test device"];
[device setOperatingSystem:@"linux"];
[device setOperatingSystemVersion:@"1"];

NSError *error;
NSData *deviceData = [device getSerializedDataWithError:&error];
[urlRequest setHTTPBody:deviceData];

MSURLSessionDataTask *meDataTask = [httpClient dataTaskWithRequest:urlRequest 
    completionHandler: ^(NSData *data, NSURLResponse *response, NSError *nserror) {

        //Request Completed

}];

[meDataTask execute];

```