---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 42766bd88a9964ff6c14cb78af0cec5e852426d6
ms.sourcegitcommit: 60ced1be6ed8dd2d23263090a1cfbc16689bb043
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/28/2020
ms.locfileid: "48782735"
---
```objc

MSHTTPClient *httpClient = [MSClientFactory createHTTPClientWithAuthenticationProvider:authenticationProvider];

NSString *MSGraphBaseURL = @"https://graph.microsoft.com/beta/";
NSMutableURLRequest *urlRequest = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:[MSGraphBaseURL stringByAppendingString:@"/print/shares/{id}/jobs"]]];
[urlRequest setHTTPMethod:@"POST"];
[urlRequest setValue:@"application/json" forHTTPHeaderField:@"Content-Type"];

MSGraphPrintJob *printJob = [[MSGraphPrintJob alloc] init];
MSGraphPrintJobConfiguration *configuration = [[MSGraphPrintJobConfiguration alloc] init];
[configuration setFeedOrientation: [MSGraphPrinterFeedOrientation longEdgeFirst]];
NSMutableArray *pageRangesList = [[NSMutableArray alloc] init];
MSGraphIntegerRange *pageRanges = [[MSGraphIntegerRange alloc] init];
[pageRanges setStart: 1];
[pageRanges setEnd: 1];
[pageRangesList addObject: pageRanges];
[configuration setPageRanges:pageRangesList];
[configuration setQuality: [MSGraphPrintQuality medium]];
[configuration setDpi: 600];
[configuration setOrientation: [MSGraphPrintOrientation landscape]];
[configuration setCopies: 1];
[configuration setDuplexMode: [MSGraphPrintDuplexMode oneSided]];
[configuration setColorMode: [MSGraphPrintColorMode blackAndWhite]];
[configuration setInputBin:@"by-pass-tray"];
[configuration setOutputBin:@"output-tray"];
[configuration setMediaSize:@"A4"];
MSGraphPrintMargin *margin = [[MSGraphPrintMargin alloc] init];
[margin setTop: 0];
[margin setBottom: 0];
[margin setLeft: 0];
[margin setRight: 0];
[configuration setMargin:margin];
[configuration setMediaType:@"stationery"];
[configuration setFinishings: null];
[configuration setPagesPerSheet: 1];
[configuration setMultipageLayout: [MSGraphPrintMultipageLayout clockwiseFromBottomLeft]];
[configuration setCollate: false];
[configuration setScaling: [MSGraphPrintScaling shrinkToFit]];
[configuration setFitPdfToPage: false];
[printJob setConfiguration:configuration];

NSError *error;
NSData *printJobData = [printJob getSerializedDataWithError:&error];
[urlRequest setHTTPBody:printJobData];

MSURLSessionDataTask *meDataTask = [httpClient dataTaskWithRequest:urlRequest 
    completionHandler: ^(NSData *data, NSURLResponse *response, NSError *nserror) {

        //Request Completed

}];

[meDataTask execute];

```