---
title: tipo de recurso chatMessageAttachment
description: Representa um anexo a uma entidade de mensagem de chat.
localization_priority: Normal
doc_type: resourcePageType
ms.prod: microsoft-teams
author: nkramer
ms.openlocfilehash: 0b6cf799de05a7e1e816fe002280d51beb18c9ce
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/18/2020
ms.locfileid: "48059142"
---
# <a name="chatmessageattachment-resource-type"></a>tipo de recurso chatMessageAttachment

Namespace: microsoft.graph

Representa um anexo a uma entidade [chat](./chatmessage.md) .

## <a name="properties"></a>Propriedades
| Propriedade  | Tipo | Descrição|
|:---------------|:--------|:----------|
|id|cadeia de caracteres| Somente leitura. ID exclusiva do anexo.|
|contentType| string | O tipo de mídia do anexo de conteúdo. Ele pode ter os seguintes valores: <br><ul><li>referência: o anexo é um link para outro arquivo. Preencha o contentURL com o link para o objeto.<br></li><li>arquivo: anexo de arquivo bruto. Preencha o campo contenturl com a codificação base64 do arquivo no formato Data:.<br></li><li>Image/: tipo de imagem com o tipo de imagem especificado por exemplo: image/png, image/jpeg, image/gif. Preencha o campo contentUrl com a codificação base64 do arquivo no formato Data:.<br></li><li>vídeo/: tipo de vídeo com o formato especificado. Ex: Video/MP4. Preencha o campo contentUrl com a codificação base64 do arquivo no formato Data:.<br></li><li>Audio/: tipo de áudio com o formato especificado. Ex: Audio/WMW. Preencha o campo contentUrl com a codificação base64 do arquivo no formato Data:.<br></li><li>tipo de cartão/aplicativo: tipo de anexo de cartão avançado com o tipo de cartão especificando o formato de cartão exato a ser usado. Defina o conteúdo com o formato JSON do cartão. Os valores com suporte para o tipo de cartão incluem:<br><ul><li>application/vnd. Microsoft. Card. Adaptive: um cartão rico que pode conter qualquer combinação de texto, fala, imagem, botões e campos de entrada. Defina a propriedade de conteúdo como, um objeto AdaptiveCard.</li><li>application/vnd. Microsoft. Card. Animation: um cartão rico que reproduz animação. Defina a propriedade de conteúdo para um AnimationCardobject.</li><li>application/vnd. Microsoft. Card. Audio: um cartão avançado que reproduz arquivos de áudio. Defina a propriedade de conteúdo, para um objeto AudioCard.</li><li>application/vnd. Microsoft. Card. Video: um cartão avançado que reproduz vídeos. Defina a propriedade de conteúdo para um objeto VideoCard.</li><li>application/vnd. Microsoft. Card. herói: um cartão herói. Defina a propriedade Content como um objeto HeroCard.</li><li>application/vnd. Microsoft. Card. Thumbnail: um cartão de miniaturas. Defina a propriedade Content como um objeto ThumbnailCard.</li><li>application/vnd. Microsoft. com. Card. recibo: um cartão de recibo. Defina a propriedade Content como um objeto ReceiptCard.</li><li>application/vnd. Microsoft. com. Card. signem: um cartão de entrada do usuário. Defina a propriedade Content como um objeto SignInCard.</ul></ul>|
|contentUrl|string|URL para o conteúdo do anexo. Protocolos suportados: http, HTTPS, File e data.|
|conteúdo|string|O conteúdo do anexo. Se o anexo for um cartão rico, defina a propriedade com o objeto ficha avançada. Essa propriedade e contentUrl são mutuamente exclusivas.|
|nome|string|Nome do anexo.|
|thumbnailUrl| string |URL para uma imagem em miniatura que o canal pode usar se oferecer suporte ao uso de um formato de conteúdo ou de uma alternativa menor ou contentUrl. Por exemplo, se você definir contentType como Application/Word e definir contentUrl como o local do documento do Word, você pode incluir uma imagem em miniatura que representa o documento. O canal pode exibir a imagem em miniatura em vez do documento. Quando o usuário clica na imagem, o canal abre o documento.|

## <a name="json-representation"></a>Representação JSON
 Veja a seguir uma representação JSON do recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "thumbnailUrl",
    "content",
    "contentUrl"
  ],
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.chatMessageAttachment"
}-->

```json
{
  "id": "string (identifier)",
  "contentType": "string",
  "contentUrl": "string",
  "content": "string",
  "name": "string",
  "thumbnailUrl": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "chat attachment resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->

