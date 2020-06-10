---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: cf05e6a258d8ae95cfa720849a4a5bdba119632d
ms.sourcegitcommit: c650b95ef4d0c3e93e2eb36cd6b52ed31200164f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/10/2020
ms.locfileid: "44684289"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var attachment = new ReferenceAttachment
{
    Name = "Personal pictures",
    SourceUrl = "https://contoso.com/personal/mario_contoso_net/Documents/Pics",
    ProviderType = ReferenceAttachmentProvider.OneDriveConsumer,
    Permission = ReferenceAttachmentPermission.Edit,
    IsFolder = true
};

await graphClient.Me.Events["AAMkAGE1M88AADUv0uAAAG="].Attachments
    .Request()
    .AddAsync(attachment);

```