---
author: ananmishr
description: O recurso Audio agrupa propriedades relacionadas a áudio em um item em uma estrutura simples.
ms.date: 09/10/2017
title: Áudio
localization_priority: Normal
ms.prod: microsoft-teams
doc_type: resourcePageType
ms.openlocfilehash: 146d9730c0a1c4e73ac16815abddd37eb729545b
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/18/2020
ms.locfileid: "48034200"
---
# <a name="audio-facet"></a>Faceta Audio

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

O recurso **Audio** agrupa propriedades relacionadas a áudio em um item em uma estrutura simples.

Se um [**DriveItem**](driveitem.md) tiver uma faceta **audio** não nula, o item representará um arquivo de áudio. As propriedades do recurso **Áudio** são preenchidas extraindo-se os metadados do arquivo. 

## <a name="json-representation"></a>Representação JSON

<!-- { "blockType": "resource", "@odata.type": "microsoft.graph.audio" } -->
```json
{
  "album": "string",
  "albumArtist": "string",
  "artist": "string",
  "bitrate": 128,
  "composers": "string",
  "copyright": "string",
  "disc": 0,
  "discCount": 0,
  "duration": 567,
  "genre": "string",
  "hasDrm": false,
  "isVariableBitrate": false,
  "title": "string",
  "track": 1,
  "trackCount": 16,
  "year": 2014
}
```

## <a name="properties"></a>Propriedades

| Nome da propriedade         | Tipo    | Descrição                                                          |
|:----------------------|:--------|:---------------------------------------------------------------------|
| **album**             | string  | O título do álbum deste arquivo de áudio.                          |
| **albumArtist**       | string  | Artista nomeado no álbum para o arquivo de áudio.                    |
| **artist**            | string  | O artista do arquivo de áudio.                            |
| **bitrate**           | Int32   | Taxa de bits expressa em kbps.                                           |
| **composers**         | string  | O nome do compositor do arquivo de áudio.                          |
| **copyright**         | string  | Informações de direitos autorais para o arquivo de áudio.                            |
| **disc**              | Int32   | O número do disco do qual este arquivo de áudio é proveniente.                    |
| **discCount**         | Int32   | O número total de discos neste álbum.                             |
| **duration**          | Int64   | Duração do arquivo de áudio, expressa em milissegundos                |
| **genre**             | string  | O gênero deste arquivo de áudio.                                        |
| **hasDrm**            | booliano | Indica se o arquivo está protegido com o gerenciamento de direitos digitais.   |
| **isVariableBitrate** | booliano | Indica se o arquivo é codificado com uma taxa de bits variável.            |
| **title**             | string  | O título do arquivo de áudio.                                         |
| **track**             | Int32   | O número da faixa no disco original para este arquivo de áudio.    |
| **trackCount**        | Int32   | O número total de faixas no disco original para este arquivo de áudio. |
| **year**              | Int32   | O ano em que o arquivo de áudio foi gravado.                                |

[item-resource]: ../resources/driveitem.md

## <a name="remarks"></a>Comentários

Para saber mais sobre as facetas de um DriveItem, confira [DriveItem](driveitem.md).

<!--
{
  "type": "#page.annotation",
  "description": "The audio facet provides information about music or audio metadata.",
  "keywords": "music,audio,metadata,onedrive",
  "section": "documentation",
  "tocPath": "Facets/Audio",
  "suppressions": []
}
-->


