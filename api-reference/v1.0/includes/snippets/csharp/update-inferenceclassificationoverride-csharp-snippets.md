---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 01852563a2e17275dfee2155b3124408772940cf
ms.sourcegitcommit: af4b2fc18449c33979cf6d75bd680f40602ba708
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "48622544"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var inferenceClassificationOverride = new InferenceClassificationOverride
{
    ClassifyAs = InferenceClassificationType.Focused
};

await graphClient.Me.InferenceClassification.Overrides["{id}"]
    .Request()
    .UpdateAsync(inferenceClassificationOverride);

```