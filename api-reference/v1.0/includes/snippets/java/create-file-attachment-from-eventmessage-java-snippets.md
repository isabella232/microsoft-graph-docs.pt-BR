---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: ac872eeac24c606ec4b10d891e6c8c756f8cbfd7
ms.sourcegitcommit: b18f978808fef800bff9e587464a5f3e18eb7687
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/25/2019
ms.locfileid: "35888269"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

Attachment attachment = new Attachment();
attachment.additionalDataManager().put("@odata.type", new JsonPrimitive("microsoft.graph.fileAttachment"));
attachment.name = "name-value";
attachment.contentType = "contentType-value";
attachment.isInline = false;
attachment.contentLocation = "contentLocation-value";
attachment.contentBytes = "base64-contentBytes-value";

graphClient.me().messages("{id}").attachments()
    .buildRequest()
    .post(attachment);

```