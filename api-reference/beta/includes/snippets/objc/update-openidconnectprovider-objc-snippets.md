---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: df3cc3f2f0abd4c3aef36c34625af030e105a18e
ms.sourcegitcommit: 496410c1e256aa093eabf27f17e820d9ee91a293
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/05/2020
ms.locfileid: "46566670"
---
```objc

MSHTTPClient *httpClient = [MSClientFactory createHTTPClientWithAuthenticationProvider:authenticationProvider];

NSString *MSGraphBaseURL = @"https://graph.microsoft.com/beta/";
NSMutableURLRequest *urlRequest = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:[MSGraphBaseURL stringByAppendingString:@"/identityProviders/OIDC-V1-MyTest-085a8a0c-58cb-4b6d-8e07-1328ea404e1a"]]];
[urlRequest setHTTPMethod:@"PATCH"];
[urlRequest setValue:@"application/json" forHTTPHeaderField:@"Content-Type"];

MSGraphIdentityProvider *identityProvider = [[MSGraphIdentityProvider alloc] init];
[identityProvider setResponseType: [MSGraphOpenIdConnectResponseTypes id_token]];

NSError *error;
NSData *identityProviderData = [identityProvider getSerializedDataWithError:&error];
[urlRequest setHTTPBody:identityProviderData];

MSURLSessionDataTask *meDataTask = [httpClient dataTaskWithRequest:urlRequest 
    completionHandler: ^(NSData *data, NSURLResponse *response, NSError *nserror) {

        //Request Completed

}];

[meDataTask execute];

```