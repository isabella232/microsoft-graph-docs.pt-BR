---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 900e6e36cc8362d504d69f2c57d6ef9911da7438
ms.sourcegitcommit: 5a1373f2ccd9ee813fc60d42e7ac6b115b5f9f66
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/21/2020
ms.locfileid: "44336361"
---
```objc

MSHTTPClient *httpClient = [MSClientFactory createHTTPClientWithAuthenticationProvider:authenticationProvider];

NSString *MSGraphBaseURL = @"https://graph.microsoft.com/v1.0/";
NSMutableURLRequest *urlRequest = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:[MSGraphBaseURL stringByAppendingString:@"/places/Building1RroomList@contoso.onmicrosoft.com"]]];
[urlRequest setHTTPMethod:@"PATCH"];
[urlRequest setValue:@"application/json" forHTTPHeaderField:@"Content-Type"];

MSGraphPlace *place = [[MSGraphPlace alloc] init];
[place setDisplayName:@"Building 1"];
[place setPhone:@"555-555-0100"];
MSGraphPhysicalAddress *address = [[MSGraphPhysicalAddress alloc] init];
[address setStreet:@"4567 Main Street"];
[address setCity:@"Buffalo"];
[address setState:@"NY"];
[address setPostalCode:@"98052"];
[address setCountryOrRegion:@"USA"];
[place setAddress:address];
MSGraphOutlookGeoCoordinates *geoCoordinates = [[MSGraphOutlookGeoCoordinates alloc] init];
[geoCoordinates setAltitude: null];
[geoCoordinates setLatitude: 47.0];
[geoCoordinates setLongitude: -122.0];
[geoCoordinates setAccuracy: null];
[geoCoordinates setAltitudeAccuracy: null];
[place setGeoCoordinates:geoCoordinates];

NSError *error;
NSData *placeData = [place getSerializedDataWithError:&error];
[urlRequest setHTTPBody:placeData];

MSURLSessionDataTask *meDataTask = [httpClient dataTaskWithRequest:urlRequest 
    completionHandler: ^(NSData *data, NSURLResponse *response, NSError *nserror) {

        //Request Completed

}];

[meDataTask execute];

```