---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 39517b88381c256ac2c755813c5eac41871108bf
ms.sourcegitcommit: c650b95ef4d0c3e93e2eb36cd6b52ed31200164f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/10/2020
ms.locfileid: "44684611"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var threatAssessmentRequest = new FileAssessmentRequestObject
{
    ExpectedAssessment = ThreatExpectedAssessment.Block,
    Category = ThreatCategory.Malware,
    FileName = "test.txt",
    ContentData = "VGhpcyBpcyBhIHRlc3QgZmlsZQ=="
};

await graphClient.InformationProtection.ThreatAssessmentRequests
    .Request()
    .AddAsync(threatAssessmentRequest);

```