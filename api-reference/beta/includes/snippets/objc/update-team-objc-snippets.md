---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 9f8bf8f838d7f72d8007e4be3bce52dcbc20227f
ms.sourcegitcommit: a6d284b3726139f11194aa3d23b8bb79165cc09e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "46813652"
---
```objc

MSHTTPClient *httpClient = [MSClientFactory createHTTPClientWithAuthenticationProvider:authenticationProvider];

NSString *MSGraphBaseURL = @"https://graph.microsoft.com/beta/";
NSMutableURLRequest *urlRequest = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:[MSGraphBaseURL stringByAppendingString:@"/teams/{id}"]]];
[urlRequest setHTTPMethod:@"PATCH"];
[urlRequest setValue:@"application/json" forHTTPHeaderField:@"Content-Type"];

MSGraphTeam *team = [[MSGraphTeam alloc] init];
[team setIsMembershipLimitedToOwners: true];
MSGraphTeamMemberSettings *memberSettings = [[MSGraphTeamMemberSettings alloc] init];
[memberSettings setAllowCreateUpdateChannels: true];
[team setMemberSettings:memberSettings];
MSGraphTeamMessagingSettings *messagingSettings = [[MSGraphTeamMessagingSettings alloc] init];
[messagingSettings setAllowUserEditMessages: true];
[messagingSettings setAllowUserDeleteMessages: true];
[team setMessagingSettings:messagingSettings];
MSGraphTeamFunSettings *funSettings = [[MSGraphTeamFunSettings alloc] init];
[funSettings setAllowGiphy: true];
[funSettings setGiphyContentRating: [MSGraphGiphyRatingType strict]];
[team setFunSettings:funSettings];
MSGraphTeamDiscoverySettings *discoverySettings = [[MSGraphTeamDiscoverySettings alloc] init];
[discoverySettings setShowInTeamsSearchAndSuggestions: true];
[team setDiscoverySettings:discoverySettings];

NSError *error;
NSData *teamData = [team getSerializedDataWithError:&error];
[urlRequest setHTTPBody:teamData];

MSURLSessionDataTask *meDataTask = [httpClient dataTaskWithRequest:urlRequest 
    completionHandler: ^(NSData *data, NSURLResponse *response, NSError *nserror) {

        //Request Completed

}];

[meDataTask execute];

```