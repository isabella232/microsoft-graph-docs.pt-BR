---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: d6ae7a4c407098c7728ad21110284905ab0133a8
ms.sourcegitcommit: 60dfb2ad9ef17f2918c4ee34ebb74f63e32ce2d3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/05/2019
ms.locfileid: "37996975"
---
```objc

MSHTTPClient *httpClient = [MSClientFactory createHTTPClientWithAuthenticationProvider:authenticationProvider];

NSString *MSGraphBaseURL = @"https://graph.microsoft.com/beta/";
NSMutableURLRequest *urlRequest = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:[MSGraphBaseURL stringByAppendingString:@"/me/profile/anniversaries"]]];
[urlRequest setHTTPMethod:@"GET"];

MSURLSessionDataTask *meDataTask = [httpClient dataTaskWithRequest:urlRequest 
    completionHandler: ^(NSData *data, NSURLResponse *response, NSError *nserror) {

        NSError *jsonError = nil;
        NSDictionary *jsonFinal = [NSJSONSerialization JSONObjectWithData:data options:0 error:&jsonError];
        NSMutableArray *personAnniversaryList = [[NSMutableArray alloc] init];
        personAnniversaryList = [jsonFinal valueForKey:@"value"];
        MSGraphPersonAnniversary *personAnniversary = [[MSGraphPersonAnniversary alloc] initWithDictionary:[personAnniversaryList objectAtIndex: 0] error:&nserror];

}];

[meDataTask execute];

```