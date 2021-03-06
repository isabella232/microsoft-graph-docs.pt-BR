---
title: tipo de recurso participante
description: O tipo de participante.
author: ananmishr
localization_priority: Normal
ms.prod: cloud-communications
doc_type: resourcePageType
ms.openlocfilehash: 7598171b4d706a639a11d425ffa409e25126dcf8
ms.sourcegitcommit: d12bd5435c198bcd096e1f7f6a2716f4a04631cc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/19/2020
ms.locfileid: "48137145"
---
# <a name="participant-resource-type"></a>tipo de recurso participante

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Representa um participante em uma chamada.

## <a name="methods"></a>Métodos

| Método                                                 | Tipo de retorno                                                 | Descrição                                    |
|:-------------------------------------------------------|:------------------------------------------------------------|:-----------------------------------------------|
| [Lista de participantes](../api/participant-get.md)         | [participante](participant.md)                               | Recupere uma lista de objetos **participantes** na chamada. |
| [Obter participante](../api/participant-get.md)           | [participante](participant.md)                               | Leia as propriedades do objeto **participante** . |
| [Excluir participante](../api/participant-delete.md)     | Nenhum   | Excluir um participante de uma chamada.                  |
| [ConfigureMixer](../api/participant-configuremixer.md) | [commsOperation](commsoperation.md)                         | Configure o mixer de áudio do participante.         |
| [Convidar](../api/participant-invite.md)                 | [inviteParticipantsOperation](../resources/inviteparticipantsoperation.md)                         | Convidar um participante para a chamada.              |
| [Ativar mudo para participante](../api/participant-mute.md)         | [muteParticipantOperation](muteparticipantoperation.md)     | Tirar o áudio de um participante em uma chamada.                  |
| [Ativar mudo para todos os participantes](../api/participant-muteall.md) | [commsOperation](commsoperation.md) | Ativar mudo de todos os participantes da reunião.      |

## <a name="properties"></a>Propriedades

| Propriedade             | Tipo                                     | Descrição                                                  |
| :------------------- | :--------------------------------------- | :------------------------------------------------------------|
| id                   | Cadeia de caracteres                                   | A ID do participante.                                          |
| informações                  | [participantInfo](participantinfo.md)    | O participante do participante.                          |
| isInLobby            | Booliano                                  | `true` Se o participante estiver no lobby.                          |
| IsMuted              | Booliano                                  | `true` Se o participante estiver com mudo ativado (cliente ou servidor sem som).    |
| mediaStreams         | coleção [mediaStream](mediastream.md) | A lista de fluxos de mídia.                                   |
| los             | Cadeia de caracteres                                   | Um blob de dados fornecido pelo participante na lista.     |
| recordingInfo        | [recordingInfo](recordinginfo.md)        | Informações sobre o fato de o participante ter capacidade de gravação. |

## <a name="relationships"></a>Relações
Nenhum

## <a name="json-representation"></a>Representação JSON

Veja a seguir uma representação JSON do recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.participant"
}-->
```json
{
  "id": "String (identifier)",
  "info": {"@odata.type": "#microsoft.graph.participantInfo"},
  "isInLobby": true,
  "isMuted": true,
  "mediaStreams": [ { "@odata.type": "#microsoft.graph.mediaStream" } ],
  "metadata": "String",
  "recordingInfo": { "@odata.type": "#microsoft.graph.recordingInfo" }
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "participant resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->


