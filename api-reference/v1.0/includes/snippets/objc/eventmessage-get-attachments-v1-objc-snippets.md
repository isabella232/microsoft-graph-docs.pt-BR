---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 80a190c54f1be7e3e827516f4924dde8f066a5b2
ms.sourcegitcommit: f50b1feff72182d1e19bfa346304beaf29558b68
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2019
ms.locfileid: "36461730"
---
```objc

MSHTTPClient *httpClient = [MSClientFactory createHTTPClientWithAuthenticationProvider:authenticationProvider];

NSString *MSGraphBaseURL = @"https://graph.microsoft.com/v1.0/";
NSMutableURLRequest *urlRequest = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:[MSGraphBaseURL stringByAppendingString:@"/me/messages/{id}/attachments"]]];
[urlRequest setHTTPMethod:@"GET"];

MSURLSessionDataTask *meDataTask = [httpClient dataTaskWithRequest:urlRequest 
    completionHandler: ^(NSData *data, NSURLResponse *response, NSError *nserror) {

        NSError *jsonError = nil;
        NSDictionary *jsonFinal = [NSJSONSerialization JSONObjectWithData:data options:0 error:&jsonError];
        NSMutableArray *attachmentList = [[NSMutableArray alloc] init];
        attachmentList = [jsonFinal valueForKey:@"value"];
        MSGraphAttachment *attachment = [[MSGraphAttachment alloc] initWithDictionary:[attachmentList objectAtIndex: 0] error:&nserror];

}];

[meDataTask execute];

```